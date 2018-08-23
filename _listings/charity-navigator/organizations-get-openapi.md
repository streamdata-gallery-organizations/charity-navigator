---
swagger: "2.0"
x-collection-name: Charity Navigator
x-complete: 0
info:
  title: Charity Navigator Get Organizations
  description: |-
    Retrieve a list of the organizations available in the Charity Navigator Data
    Store. Allows paged retrieval, simple and advanced searching.
  version: 1.0.0
host: api.data.charitynavigator.org
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Organizations:
    get:
      summary: Get Organizations
      description: |-
        Retrieve a list of the organizations available in the Charity Navigator Data
        Store. Allows paged retrieval, simple and advanced searching.
      operationId: searchOrganizations
      x-api-path-slug: organizations-get
      parameters:
      - in: query
        name: app_id
        description: '3Scale App ID: unique identifier for an application registered
          in theCharity Navigator  developer portal'
      - in: query
        name: app_key
        description: '3Scale App Key: a secret key to authenticate the assigned App
          ID'
      - in: query
        name: categoryID
        description: ID of a Category
      - in: query
        name: causeID
        description: ID of a Cause
      - in: query
        name: cfcCharities
        description: Specifies whether to include or exclude organizations that are
          included inthe Combined Federal Campaign, the largest workplace giving campaign
          in USA
      - in: query
        name: city
        description: Filters search results to include only organizations in cities
          whose namesmatch the specified string
      - in: query
        name: donorPrivacy
        description: Specifies whether to include or exclude organizations that have
          a donorprivacy policy
      - in: query
        name: fundraisingOrgs
        description: Specifies whether to include or exclude organizations flagged
          by CharityNavigator as fundraising organizations
      - in: query
        name: maxRating
        description: Filters search results to include only organizations with a rating
          less thanor equal to the specified value
      - in: query
        name: minRating
        description: Filters search results to include only organizations with a rating
          greaterthan or equal to the specified value
      - in: query
        name: noGovSupport
        description: Specifies whether to include or exclude organizations that do
          not receivegovernment support
      - in: query
        name: pageNum
        description: Page number to return, in case the number of available objects
          in the resultset is greater than the specified or default `pageSize`
      - in: query
        name: pageSize
        description: Number of organizations to return in a single response message
      - in: query
        name: rated
        description: Specifies whether to include only rated charities or unrated
          charities
      - in: query
        name: scopeOfWork
        description: Filters search results to include only organizations with a given
          scope ofwork
      - in: query
        name: search
        description: A simple search string that narrows the results to organizations
          matchingthe specified search terms
      - in: query
        name: searchType
        description: Used in combination with the `search` parameter, specifies the
          type ofsearch to be performed
      - in: query
        name: sizeRange
        description: Filters search results to include only organizations within a
          given sizebracket, as measured in annual Total Expenses
      - in: query
        name: sort
        description: Specifies how results should be sorted
      - in: query
        name: state
        description: If set to a valid 2-letter state code (not case-sensitive), filters
          searchresults to include only organizations in the specified state
      - in: query
        name: zip
        description: Filters search results to include only organizations in the specified
          zipcode
      responses:
        200:
          description: OK
      tags:
      - Organizations
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---