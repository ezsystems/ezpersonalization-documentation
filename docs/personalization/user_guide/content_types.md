# 5. Content Types

In the **advanced** edition of the recommendation engine it is possible to build different recommendation domains. It can be achieved by splitting all the products into different content types. There are several possible use cases for content types.

- A publisher tracks articles, pictures and videos as three different types.
- A supermarket splits all the products into food and non-food product groups.
- An owner of several web shops uses a single account for all of them

The content types concept provides the possibility to make so-called cross domain recommendations (like "Users who watched this film also read this book" or "Users who read this article also liked these photos").

Additionally to the logical separation of the content domains the content types provide another important advantage. They play a role if different types of products are not equally popular but must be recommended equally often. For example, on a publisher's page users watch videos less often than they read articles. If the most popular products are requested without content type splitting, there will be most likely no videos in the result. If articles and videos are split into different content types, it is possible to explicitly request popular videos and/or popular articles.

Below is a comparison for different ways of splitting content in the recommendation engine.

|Use case|content types solution (domain context)|Attribute based sub-models (group context)|Different recommendation engine accounts|
|---|---|---|---|
|Cross-group recommendation requests are possible|yes|yes|no|
|Products must belong to one group|mandatory|optional|mandatory|
|Products can belong to multiple groups|no|yes|no|
|Single recommendation request can contain products from different groups|no|yes|no|
|Product can change the group it belongs to|no|yes|no|
|Different content types share the scenario and model configuration|yes|yes|no|
|Required Recommender Edition|single advanced|-|multiple basic|

#### Scenario configuration

If multiple content types are enabled, one must enable this output type for every scenario that should recommend this type.

![Scenario settings](../img/scenario_configuration.png)

Every scenario supports a single input type and multiple output types (see [8. Scenarios](scenarios.md)). Every recommendation request delivers only content of one output content type (even if multiple are selected in the interface above). The output type is set during the recommendation request and must be covered by the list of the supported content types in the requested scenario.

You can find more information about fetching recommendations in developer documentation: [Recommendation API](../developer_guide/recommendation_api.md)
