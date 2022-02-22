# Quick start

## oAuth 2
This API uses the oAuth2 authorisation model, learn more about it here.
Learn how to make authenticated requests here.

## Client registration
If you are creating an application and you want to use these APIs, you'll need to sign-up to the platform as a developer and register a new application on your dashboard. After the registration is completed you will be given a secret and a client id, you'll use that to authenticate your user on our platform. You must define a safe redirect url, this will be the only url allowed for your application authentication.

## Pagination
Pagination is off by default for agent user, otherwise if he is an admin or a collaborator, pagination will be turned on automatically. You can also activate programmatically the pagination system, just define the page parameter in GET requests. (recommended)
## Response object
    {
        "total": 50,
        "per_page": 15,
        "current_page": 1,
        "last_page": 4,
        "first_page_url": "http://example.app?page=1",
        "last_page_url": "http://example.app?page=4",
        "next_page_url": "http://example.app?page=2",
        "prev_page_url": null,
        "path": "http://example.app",
        "from": 1,
        "to": 15,
        "data":[
                //Result array
        ]
    }

## Response metadata
In order to access quick aggregate values, such as total sums and more, you have to make a paginated request with the metadata parameter set.
This only works for paginated response and, temporary, just for invoices requests.

## Timestamps
In this API we use timestamps to track creation and update time. By default, timestamps are added to every model that use time tracking. Response structure is as follows:

    {
        ...
        "created_at": "2019-01-01 01:01:01",
        "updated_at": "2019-01-01 01:01:01"
    }

## Ordering and filtering
In most of our API methods you can pass an additional parameters to manage order index and direction. 
Just set sort with the name of the field you want to use in order to control order flow. Use the negative sign ( - ) to change the order direction to desc.
If you want to apply a filter, just set the filter array in the request params following the structure filter[name]=value1,value2

Ordering and filtering are available for Customers and Orders, at the moment