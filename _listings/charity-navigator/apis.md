---
name: Charity Navigator
x-slug: charity-navigator
description: Charity Navigator is an American independent charity watchdog organization
  that evaluates charitable organizations in the United States.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
x-kinRank: "7"
x-alexaRank: "49197"
tags: Charity Navigator
created: "2018-08-26"
modified: "2018-08-26"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/apis.md
specificationVersion: "0.14"
apis:
- name: CharityNavigatorDataAPI - Get Organizations
  x-api-slug: organizations-get
  description: |-
    Retrieve a list of the organizations available in the Charity Navigator Data
    Store. Allows paged retrieval, simple and advanced searching.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizations-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizations-get-openapi.md
- name: CharityNavigatorDataAPI - Get Organizations Ein
  x-api-slug: organizationsein-get
  description: |-
    Retrieve full detail of a single Organization. This is a composite set of
    information describing an organization that may engage in charitable work.
    Normally the Organization data structure includes a single legal entity, though
    legal entity information may be excluded in exceptional cases.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizationsein-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizationsein-get-openapi.md
- name: CharityNavigatorDataAPI - Get Organizations Ein Ratings Rating
  x-api-slug: organizationseinratingsratingid-get
  description: |-
    Retrieve a single Rating object for an Organization. Each rating is listed
    once, under its primary `referenceOrganization`. Note that the rating may apply
    to other organizations, and this is represented by `includedOrganizations`,
    which is a collection of hyperlinks to all of the organizations to which the
    rating applies.
    The rating is a point-in-time assessment provided by Charity Navigator, along
    with related metrics and ratios taken from financial statements for a fiscal
    year, on which the rating is based. <br/> ![Content
    Subscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png
    "Included with the paid Content Subscription.")
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizationseinratingsratingid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizationseinratingsratingid-get-openapi.md
- name: CharityNavigatorDataAPI - Get Organizations Ein Advisories
  x-api-slug: organizationseinadvisories-get
  description: |-
    Retrieve the full set of Charity Navigator advisories for a specified
    organization. An advisory is a cautionary communication from Charity Navigator,
    advising of unusual events or behavior related to a known organization.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizationseinadvisories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/organizationseinadvisories-get-openapi.md
- name: CharityNavigatorDataAPI - Get Lists List
  x-api-slug: listslistid-get
  description: |-
    Retrieve a curated or generated list of organizations, published by Charity
    Navigator. <br/> ![Content
    Subscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png
    "Included with the paid Content Subscription.")
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/listslistid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/listslistid-get-openapi.md
- name: CharityNavigatorDataAPI - Get Categories
  x-api-slug: categories-get
  description: |-
    Returns metadata for Charity Navigator's classification hierarchy for
    charitable Organizations. Category is the top-level classifier, and each
    category may contain a number of Causes. <br/> ![Content
    Subscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png
    "Included with the paid Content Subscription.")
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/categories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/categories-get-openapi.md
- name: CharityNavigatorDataAPI - Get Advisory
  x-api-slug: advisory-get
  description: |-
    Retrieve the full set of Charity Navigator advisories for a specified
    organization. An advisory is a cautionary communication from Charity Navigator,
    advising of unusual events or behavior related to a known organization.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28893-www-charitynavigator-org.jpg
  humanURL: http://www.charitynavigator.org
  baseURL: https://api.data.charitynavigator.org//v2
  tags: Charities, Giving, General Data
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/advisory-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/charity-navigator/master/_listings/charity-navigator/advisory-get-openapi.md
x-common:
- type: x-blog-rss
  url: http://blog.charitynavigator.org/feeds/posts/default?alt=rss
- type: x-developer
  url: https://charity.3scale.net/
- type: x-documentation
  url: https://charity.3scale.net/docs/data-api/reference
- type: x-github
  url: https://github.com/CharityNavigator
- type: x-support
  url: https://charity.3scale.net/support
- type: x-website
  url: http://www.charitynavigator.org
- type: x-api-gallery
  url: http://capital.one.devexchange.api.gallery.streamdata.io
- type: x-api-stack
  url: http://charity.navigator.stack.network
- type: x-blog
  url: http://blog.charitynavigator.org/
- type: x-crunchbase
  url: https://crunchbase.com/organization/charity-navigator
- type: x-email
  url: helpandsupport@charitynavigator.org
- type: x-twitter
  url: https://twitter.com/CharityNav
- type: x-website
  url: https://www.charitynavigator.org
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---