{
  "info": {
    "name": "Charity Navigator Get Categories",
    "_postman_id": "46ec27bd-38a3-4e5a-9bb4-d88020860882",
    "description": "Returns metadata for Charity Navigator's classification hierarchy for\ncharitable Organizations. Category is the top-level classifier, and each\ncategory may contain a number of Causes. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizations",
      "item": [
        {
          "id": "6e678699-c0d7-4edb-becd-21cba62c7ab5",
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
              "id": "8c9a1b4d-8e9f-44ac-a9e7-8038077816fb"
            }
          ]
        },
        {
          "id": "b166e714-a498-48b0-bff0-e3516300567b",
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
              "id": "71161454-3ced-4632-a81a-2c623937522f"
            }
          ]
        },
        {
          "id": "33a99758-b61a-440c-b3b1-52153873c159",
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
              "id": "a13a9c84-98dd-44e8-afc7-c2b7ab1858dc"
            }
          ]
        },
        {
          "id": "056383d9-e2ec-4085-bfa3-2e6ce0eaab8d",
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
              "id": "46e09ee2-45c3-4c0b-98d0-2c3bbf51b5be"
            }
          ]
        },
        {
          "id": "a14cfb55-88ea-42ca-a8bd-17d8ce43d3b3",
          "name": "getAdvisories",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.data.charitynavigator.org",
              "path": [
                "v2",
                "Organizations/:ein/Advisories"
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
                },
                {
                  "key": "status",
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
            "description": "Retrieve the full set of Charity Navigator advisories for a specified\norganization. An advisory is a cautionary communication from Charity Navigator,\nadvising of unusual events or behavior related to a known organization."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "77242844-18e0-44a9-9528-5e0eb6ede727"
            }
          ]
        },
        {
          "id": "c4e87ac9-bcb3-40c5-9d3d-8b6d66a51e39",
          "name": "getAdvisory",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.data.charitynavigator.org",
              "path": [
                "v2",
                "Organizations/:ein/Advisories/:AdvisoryID"
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
                  "id": "AdvisoryID",
                  "value": "{}",
                  "type": "string"
                },
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
            "description": "Retrieve full details of a single Advisory, under a given organization. An\nadvisory is a cautionary communication from Charity Navigator, advising of\nunusual events or behavior related to a known organization."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a666d7a3-e0cc-4801-8f3e-bb2f34e9282d"
            }
          ]
        }
      ]
    },
    {
      "name": "Lists",
      "item": [
        {
          "id": "c2ad2e70-0bd1-462c-973e-ce7c5f5f1940",
          "name": "getLists",
          "request": {
            "url": "http://api.data.charitynavigator.org/v2/Lists?app_id=%7B%7D&app_key=%7B%7D&pageNum=%7B%7D&pageSize=%7B%7D",
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
            "description": "Retrieve a set of Lists defined in Charity Navigator. Each entry in this\ncollection is a curated or generated list of organizations, published by Charity\nNavigator. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f16ed61d-810f-410b-b625-354eba3a0bde"
            }
          ]
        },
        {
          "id": "97529629-2f5c-4d8f-abc7-cf6405cdbcf0",
          "name": "getList",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.data.charitynavigator.org",
              "path": [
                "v2",
                "Lists/:ListID"
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
                  "id": "ListID",
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
            "description": "Retrieve a curated or generated list of organizations, published by Charity\nNavigator. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a409a1e9-d6f4-4d10-8eb8-72b96921cdc0"
            }
          ]
        }
      ]
    },
    {
      "name": "Categories",
      "item": [
        {
          "id": "44c946a9-b09b-4e7e-a063-6811c14a8ffd",
          "name": "getCategories",
          "request": {
            "url": "http://api.data.charitynavigator.org/v2/Categories?app_id=%7B%7D&app_key=%7B%7D",
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
            "description": "Returns metadata for Charity Navigator's classification hierarchy for\ncharitable Organizations. Category is the top-level classifier, and each\ncategory may contain a number of Causes. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7ebd678e-f70a-4409-85a2-9a5e0ec96e46"
            }
          ]
        }
      ]
    }
  ]
}