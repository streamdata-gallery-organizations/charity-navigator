{
  "info": {
    "name": "Charity Navigator Get Organizations Ein Ratings Rating",
    "_postman_id": "da96748b-a0a3-4812-89a5-491903b9462d",
    "description": "Retrieve a single Rating object for an Organization. Each rating is listed\nonce, under its primary `referenceOrganization`. Note that the rating may apply\nto other organizations, and this is represented by `includedOrganizations`,\nwhich is a collection of hyperlinks to all of the organizations to which the\nrating applies.\nThe rating is a point-in-time assessment provided by Charity Navigator, along\nwith related metrics and ratios taken from financial statements for a fiscal\nyear, on which the rating is based. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizations",
      "item": [
        {
          "id": "bc100c9c-63c9-4932-b42a-2eb78259bd87",
          "name": "searchOrganizations",
          "request": {
            "url": "http://api.data.charitynavigator.org/v2/Organizations?app_id=%7B%7D&app_key=%7B%7D&categoryID=%7B%7D&causeID=%7B%7D&cfcCharities=%7B%7D&city=%7B%7D&donorPrivacy=%7B%7D&fundraisingOrgs=%7B%7D&maxRating=%7B%7D&minRating=%7B%7D&noGovSupport=%7B%7D&pageNum=%7B%7D&pageSize=%7B%7D&rated=%7B%7D&scopeOfWork=%7B%7D&search=%7B%7D&searchType=%7B%7D&sizeRange=%7B%7D&sort=%7B%7D&state=%7B%7D&zip=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a list of the organizations available in the Charity Navigator Data\nStore. Allows paged retrieval, simple and advanced searching."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9d5745a5-c0db-413e-9930-309111535240"
            }
          ]
        },
        {
          "id": "3b8fb917-dac7-43b4-8317-2c9fcc6bd433",
          "name": "getOrganization",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.data.charitynavigator.org",
              "path": [
                "v2",
                "Organizations/:ein"
              ],
              "query": [
                {
                  "key": "app_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "app_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ein",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve full detail of a single Organization. This is a composite set of\ninformation describing an organization that may engage in charitable work.\nNormally the Organization data structure includes a single legal entity, though\nlegal entity information may be excluded in exceptional cases."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cb77822d-6a98-41f3-abb0-292acd29e676"
            }
          ]
        },
        {
          "id": "ac62731a-6c04-4e9e-bbc2-a857388c1a23",
          "name": "getRatings",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.data.charitynavigator.org",
              "path": [
                "v2",
                "Organizations/:ein/Ratings"
              ],
              "query": [
                {
                  "key": "app_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "app_key",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageNum",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "pageSize",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ein",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve all Charity Navigator ratings for a single organization. <br/>\n![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ee90f23d-39f4-4d1a-ba45-0277586a322d"
            }
          ]
        },
        {
          "id": "306f8f34-c2f0-4b87-b1ab-7486f68e5098",
          "name": "getRating",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.data.charitynavigator.org",
              "path": [
                "v2",
                "Organizations/:ein/Ratings/:RatingID"
              ],
              "query": [
                {
                  "key": "app_id",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "app_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "ein",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "RatingID",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Retrieve a single Rating object for an Organization. Each rating is listed\nonce, under its primary `referenceOrganization`. Note that the rating may apply\nto other organizations, and this is represented by `includedOrganizations`,\nwhich is a collection of hyperlinks to all of the organizations to which the\nrating applies.\nThe rating is a point-in-time assessment provided by Charity Navigator, along\nwith related metrics and ratios taken from financial statements for a fiscal\nyear, on which the rating is based. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "97295710-e188-4491-ae96-9524259aa84e"
            }
          ]
        }
      ]
    }
  ]
}