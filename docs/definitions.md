# Definitions

#### Catalog

Collection of data from a database or IT System (e.g. a shop system or a CMS) that is used to display [content](#content) to the user

#### Catalog Data

[Content](#content) that is used to build the Catalog used for the Service.
The Catalog data can contain different Content Types.

####Category path

The category path is the logical path on a website which leads to the current category.
For example, if the current category is "Sandals" then the corresponding logical category path is "Women/Summer/Sandals".
You can describe it as the "path via categories to reach the content".

#### Content

Content is an abstract name of all data like products, videos, pictures, articles, blogs, etc. which constitute a Catalog.
Different content is identified by its [content type](#content-type)

#### Content Type

Content type identifies different content elements such as products, videos, pictures in the catalog.
You can e.g. have videos of content type 1 (YouTube videos) and of content type 2 (Vimeo videos).

####Context

Context is the current environment of the user.
An example could be the logical position on a website, the (current) time or the location.
It is used to enhance recommendations.

#### Explicit User Data

[User data](#user-data) that is collected from explicit feedback from the user like a rating, a "like" or a form field with some information provided

####Event Type

The type of an event. For example a click, clickrecommended, buy, rate or consume event

#### Filter

Three types of filters are available in the Recommendation Engine:

Content Filter: A filter that is applied to values of content attributes, e.g. only content with a location attribute value of "Cologne" should be recommended

User Filter: A filter that is applied to user data, e.g. do not recommend content that a user has already seen before

Boost Filter: A filter that reranks recommendations based on user attributes. The attribute's value must be available on content and users

#### Item Type

Another term for [content type](#content-type)

#### Implicit User Data

[User data](#user-data) that is collected by observing the behavior of the user with tracking of clicks or navigation through the page

#### Model

A model is an algorithm that calculates recommendations based on given [User data](#user-data)

#### Product

Product is a special type of [Content](#content)

#### Recommendation Engine

A Service that delivers recommendations based on user data and a content catalog.
Several models and filters are used to create a resulting set of recommendations.
It is a kind of an intelligent WhiteBox.

#### Recommendations

A set of content which is delivered from the Recommendation Engine as a result of a scenario configuration.

Recommendations can be delivered via multiple channels: online on a website or offline as personalized content in a newsletter.

#### Recommendation Request

A HTTP request that contains parameters as input for delivering recommendations.

#### Recommendation Box

The block which contains recommendations on a website, in a newsletter etc.

#### Scenario

A scenario is a configuration for fetching recommendation. It includes filters, the [content type](#content-type) and a prioritized list of [models](#model)

#### Submodels

Submodels are prefiltered recommendations and contain parts of the main model.
For example, only content about certain cities is included and not all content.

#### User Data

User data is all data that is collected about the user.
It can be either implicit data that is collected by tracking events like clicks, or explicit data that is collected through user feedback like using a "like" button or on a recommendation.

User data also contains attributes of the user. This could be gender, user type etc.
