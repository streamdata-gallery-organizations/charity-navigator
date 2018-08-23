{
  "info": {
    "name": "Charity Navigator Get Lists List",
    "_postman_id": "df6ac7c1-3fa9-4de3-ba45-398e067ef354",
    "description": "Retrieve a curated or generated list of organizations, published by Charity\nNavigator. <br/> ![Content\nSubscription](https://cdn2.hubspot.net/hubfs/597611/CharityNavigator/FA-Data-Table-16.png\n\"Included with the paid Content Subscription.\")",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizations",
      "item": [
        {
          "id": "80e90c75-8861-4e3a-9c5f-3a604f2524bb",
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
              "id": "4aa500e0-b9a9-448b-bab5-d97bb10f3bf9"
            }
          ]
        },
        {
          "id": "27b47b06-da3c-407e-88af-95d392e70079",
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
              "id": "0389cecd-584e-4f99-8ba9-947b531eb558"
            }
          ]
        },
        {
          "id": "cd4d87bf-57a6-4ef8-951e-54e8c2f57b2a",
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
              "id": "3566b454-cd85-409e-adc8-131f50af0def"
            }
          ]
        },
        {
          "id": "cb27c972-823c-4690-b181-53221103d4b0",
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
              "id": "813a2c9d-7384-4a2b-b851-dcb40eea9345"
            }
          ]
        },
        {
          "id": "136112ee-589d-43c0-83e7-a9574f753dbb",
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
              "id": "14d9f837-ccea-4f7f-ab04-e0a2aab9f960"
            }
          ]
        },
        {
          "id": "73504e30-e297-4e4d-a225-ad1a162a541f",
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
              "id": "34e8fd95-2012-4b3f-add5-dc541ff57bc4"
            }
          ]
        }
      ]
    },
    {
      "name": "Lists",
      "item": [
        {
          "id": "b0bf1b15-c949-4a7c-b625-a5d84aeedd6b",
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
              "id": "be3f737d-d6bd-40bc-945b-8cc95061c18c"
            }
          ]
        },
        {
          "id": "3d7ebfa6-a1d6-4bd9-a795-0edf001d7ec7",
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
              "id": "0a065faa-58ea-40e0-9bba-3892991c7866"
            }
          ]
        }
      ]
    }
  ]
}