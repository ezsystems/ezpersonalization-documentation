# 9. Content Import

Basic recommendation algorithms are statistics-based and need only the product ID and user ID. This information is provided by the event tracking as described in chapter [4. Event Types](event_types.md).
There are several use cases where the recommendation engine requires additional information linked to the products.
The most important cases are:

- Filtering results based on the category the product is located in ([Category Filter](filters.md#category-filter))
- Filtering results based on price and product availability ([General Filters](filters.md#general-filters))
- Sub-models based on custom attribute grouping ([Submodels](recommendation_models.md#submodels))
- An additional export/import interface is designed to provide editor-based models ([6. Recommendation Models](recommendation_models.md))

There are four different ways to import data into the recommendation system:

- **In-Event:** During the event tracking process, where related data is attached to a click event (e.g. categorypath information)
- **Push interface:** Classic HTTP POST-based import. It is suitable for uploading single content or editor lists
- **Pull interface:** The recommendation engine loads an exported file from the specified location in the background. It was designed to upload big portions of information, for example a weekly update of the whole product catalog
- **Trigger logic:** The recommendation engine triggers a transactional full import at the customer's system. Therefore some custom development or a plugin is needed. 

!!! tip

    You can find Specification for Import interfaces in the developer guide under [Content API](../developer_guide/content_api.md).
