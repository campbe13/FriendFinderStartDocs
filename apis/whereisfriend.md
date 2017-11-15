**Find where a friend is at a given time**
----
  Fetch the whereabouts of a given friend (based on their email) at a given time. Requires the user's authentication credentials email and password.

* **URL**

  /api/api/whereisfriend

* **Method:**
  
  `GET` 
  
*  **URL Params**

   **Required:**
 
   `email=[string]`
   `password=[string]`
   `friendemail=[string]`
   `day=[integer]`
   `time=[integer]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `{course : "420-411-DW" , section:"1"} `


  * **Code:** 200 <br />
    **Content:** `{course : "" , section:""} `
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "invalid credentials" }`

	
  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "bad or missing parameter" }`

	
  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "not a friend" }`

* **Sample Call:**

  `curl -X GET -H "Accept: application/json" "https://hostname/api/api/whereisfriend?email=j@j.j&password=123456&ffriendemail=t@t.t&day=1&time=1030"`
   
* **Notes:**

An object with empty strings is returned if the friend is not in class