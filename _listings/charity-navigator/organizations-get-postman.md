{
  "info": {
    "name": "Charity Navigator Get Organizations",
    "_postman_id": "982bcaf6-e8b1-4e86-98b2-bd91a1830bf5",
    "description": "Retrieve a list of the organizations available in the Charity Navigator Data\nStore. Allows paged retrieval, simple and advanced searching.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Organizations",
      "item": [
        {
          "id": "3b368410-ddd7-45db-b9b3-4b6950338a48",
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
              "id": "98a439b9-c9d0-4fe4-8b63-68884aa81b8b"
            }
          ]
        }
      ]
    }
  ]
}