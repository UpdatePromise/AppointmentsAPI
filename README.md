**Title**
----
  <_Additional information about your API call. Try to use verbs that match both request type (fetching vs modifying) and plurality (one vs multiple)._>

* **URL**

  <_The URL Structure (path only, no root url)_>

* **Method:**

  <_The request type_>

  `GET` | `POST` | `DELETE` | `PUT`

*  **URL Params**

   <_If URL params exist, specify them in accordance with name mentioned in URL section. Separate into optional and required. Document data constraints._>

   **Required:**

   `id=[integer]`

   **Optional:**

   `photo_id=[alphanumeric]`

* **Data Params**

  <_If making a post request, what should the body payload look like? URL Params rules apply here too._>

* **Success Response:**

  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** `{ id : 12 }`

* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

  <_Just a sample call to your endpoint in a runnable format ($.ajax call or a curl request) - this makes life easier and more predictable._>

* **Notes:**

  <_This is where all uncertainties, commentary, discussion etc. can go. I recommend timestamping and identifying oneself when leaving comments here._>

**Get Motors Years**
----

* **motors/years**

* **Method:**

  `GET`

*  **URL Params**


   **Required:**

   **Required:**

   ``

   **Optional:**

   ``

* **Data Params**


* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: years, data: [{ id : year, value : year }, ...], success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "years", data: [], success : False}`

* **Notes:**
  
**Get Motors Makes**
----

* **motors/makes/year/{year}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `year=[string]`

   **Optional:**

   ``

* **Data Params**

  <__>

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: makes, data: [{ id : 12, value : Acura }, ...], success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "makes", data: [], success : False}`

* **Notes:**
  
**Get Motors Models**
----

* **motors/models/year/{year}/make/{make}**


* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `year=[string], make=[string]`

   **Optional:**

   ``

* **Data Params**


* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: models, data: [{ id : 12, value : RSX }, ...], success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "models", data: [], success : False}`

* **Notes:**

  <__>
  
**Get Motors Trims**
----

* **motors/trims/year/{year}/make/{make}/model/{model}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `year=[string], make=[string], model=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: trims, data: [{ id : 12, value : LX }, ...], success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "trims", data: [], success : False}`

* **Notes:**

  <__>
  
**Get Motors Vehicle Image**
----

* **motors/image/year/{year}/make/{make}/model/{model}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `year=[string], make=[string], model=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: image_url, data: image_url, success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "image_url", data: [], success : False}`

* **Notes:**

**Get Motors Recommended Services**
----

* **motors/recommended_services/year/{year}/make/{make}/model/{model}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `year=[string], make=[string], model=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: recommended_services, data: [{id : 12, value : Fix Air Filter}, ...], success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "recommended_services", data: [], success : False}`

* **Notes:**

**Get Motors Recommended Services**
----

* **motors/recommended_services/year/{year}/make/{make}/model/{model}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `year=[string], make=[string], model=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{type: recommended_services, data: [{id : 12, value : Fix Air Filter}, ...], success : True}`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "recommended_services", data: [], success : False}`

* **Notes:**

**Create Customer**
----

* **dms/{company}/customer**

* **Method:**

  `POST`

*  **URL Params**

   **Required:**

   `company=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: customer, 
                   data: [{
                    "first_name": "john",
                    "last_name": "smith",
                    "mobile_phone": "(123)-456-7890",
                    "id": "10871"
                   }], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "customer", data: [], success : False}`

* **Notes:**

**Search Customer**
----

* **dms/{company}/customer/search**

* **Method:**

  `POST`

*  **URL Params**

   **Required:**

   `company=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: customer, 
                   data: [{
                    "first_name": "john",
                    "last_name": "smith",
                    "mobile_phone": "(123)-456-7890",
                    "id": "10871"
                   }, ...], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "customer", data: [], success : False}`

* **Notes:**

**Get Customer**
----

* **dms/{company}/customer/{customer}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: customer, 
                   data: [{
                    "first_name": "john",
                    "last_name": "smith",
                    "mobile_phone": "(123)-456-7890",
                    "id": "10871"
                   }, ...], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "customer", data: [], success : False}`

* **Notes:**

**Update Customer**
----

* **dms/{company}/customer/{customer}**

* **Method:**

  `POST`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: customer, 
                   data: [{
                    "first_name": "john",
                    "last_name": "smith",
                    "mobile_phone": "(123)-456-7890",
                    "id": "10871"
                   }, ...], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "customer", data: [], success : False}`

* **Notes:**

**Delete Customer**
----

* **dms/{company}/customer/{customer}**

* **Method:**

  `DELETE`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: customer, 
                   data: [], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "customer", data: [], success : False}`

* **Notes:**

**Search Customer Vehicle**
----

* **dms/{company}/customer/{customer}/vehicle/search**

* **Method:**

  `POST`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: vehicle, 
                   data: [ {
                    "trim": "None",
                    "mileage": "225600",
                    "make": "Jeep",
                    "vin": "1J4FJ68S3WL250852",
                    "year": "1998",
                    "model": "cherokee",
                    "id": "5"
                   }, ...], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "vehicle", data: [], success : False}`

* **Notes:**

**Get Customer Vehicle**
----

* **dms/{company}/customer/{customer}/vehicle/{vehicle}**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string], vehicle=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: vehicle, 
                   data: [ {
                    "trim": "None",
                    "mileage": "225600",
                    "make": "Jeep",
                    "vin": "1J4FJ68S3WL250852",
                    "year": "1998",
                    "model": "cherokee",
                    "id": "5"
                   }, ...], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "vehicle", data: [], success : False}`

* **Notes:**

**Update Customer**
----

* **dms/{company}/customer/{customer}/vehicle/{vehicle}**

* **Method:**

  `POST`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string], vehicle=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: vehicle, 
                   data: [ {
                    "trim": "None",
                    "mileage": "225600",
                    "make": "Jeep",
                    "vin": "1J4FJ68S3WL250852",
                    "year": "1998",
                    "model": "cherokee",
                    "id": "5"
                   }, ...], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "vehicle", data: [], success : False}`

* **Notes:**

**Delete Customer Vehicle**
----

* **dms/{company}/customer/{customer}/vehicle/{vehicle}**

* **Method:**

  `DELETE`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string], vehicle=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: vehicle, 
                   data: [], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "vehicle", data: [], success : False}`

* **Notes:**

**Deferred Job Codes For Customer Vehicle**
----

* **dms/{company}/customer/{customer}/vehicle/{vehicle}/deferred**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `company=[string], customer=[string], vehicle=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: vehicle, 
                   data: [{id : 13RP59X, name : Air Filter Change}], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "vehicle", data: [], success : False}`

* **Notes:**

**Get Services**
----

* **dms/{company}/services**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `company=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: services, 
                   data: [{id : 13RP59X, name : Air Filter Change}], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "services", data: [], success : False}`

* **Notes:**

**Get Employees**
----

* **dms/{company}/employees**

* **Method:**

  `GET`

*  **URL Params**

   **Required:**

   `company=[string]`

   **Optional:**

   ``

* **Data Params**

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{
                   type: employee, 
                   data: [{id : 12, name : John Snow}], 
                   success : True
                  }`

* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{type: "employee", data: [], success : False}`

* **Notes:**

