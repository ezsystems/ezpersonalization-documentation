# 10. User Data Import

By default the recommendation engine has very little information about the user visiting the website, especially first-time visitors. The only information provided in the event tracking and recommendation request is the customer ID of the website owner and an external user ID (usually an anonymous session ID). This external user ID is again anonymized in the recommendation engine by a hashing algorithm.

Sometimes it is helpful to store additional attributes for every user, for example age or home city. It is possible to retrieve the stored information based on the external user ID, but due to the hashing step mentioned above, it is not possible to get the external user ID within the user's attribute set (unless the external ID is not explicitly stored as an attribute of course).

How user attributes are imported and what they can be used for is described in the [User API](../developer_guide/user_api.md).

Usage of the user attribute in the recommendation process is quite straightforward and explained in detail in the [Recommendation API](../developer_guide/recommendation_api.md).

!!! tip

    An example of how user attributes can be used in the recommendation engine:[Boost-Filters](filters.md#boost-filters)

    Information on the import format can be found in the developer guide:[User API](../developer_guide/user_api.md)
