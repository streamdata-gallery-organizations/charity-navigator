{
  "info": {
    "name": "Charity Navigator Get Organizations Ein",
    "_postman_id": "f0608c2e-35fb-4f1d-8cfd-acd93093c32e",
    "description": "Retrieve full detail of a single Organization. This is a composite set of\ninformation describing an organization that may engage in charitable work.\nNormally the Organization data structure includes a single legal entity, though\nlegal entity information may be excluded in exceptional cases.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizations",
      "item": [
        {
          "id": "06f353aa-3965-4c1b-828b-222305b431fa",
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
              "id": "aa46b3ee-083c-4f60-b2d6-d7067ede57c4"
            }
          ]
        },
        {
          "id": "59af8ae0-54ee-4df9-babe-0c9840d90e58",
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
              "id": "88f39e4d-464e-4a99-951d-5b9d948356ff"
            }
          ]
        }
      ]
    }
  ]
}