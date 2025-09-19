# What is Pegination

django provide a few class that help you manage paginted data that data split accrose several page with previous/next

or

pagination is process of dividing a large page of data into smaller chunks or pages 
Rest Freamwork include support for customizable pagination style 


# Type of Pegination 

DRF provide Three built in pagination style
1. PageNumberPagination

    this pagination style use page number like 1|2|3|4|5|6 end more

    
2. LimitOffsetPagination

    this pagination will work with limit and off set

    limit = how many result you want (page size)
    offset = how many result to skip before startting

    exmple : 
        you have 100 users in database and you request with limit=10&offset=20
        the API will return 10 users from th starting 21stuser (becuse offset skip 20 records)

3. CursorPagination