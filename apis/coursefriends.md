**Get friends registered for a class**
----
  Fetch all friends of the user (with authentication credentials email and password), who are registered for a given class. The class is specified by course name and section.

* **URL**

  /api/api/coursefriends

* **Method:**
  
  `GET` 
  
*  **URL Params**

   **Required:**
 
   `email=[string]`
   `password=[string]`
   `coursename=[string]`
   `section=[string]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{email : "j@j.j" , firstname:"Jaya", lastname:"Nila"} ,
					{email : "t@t.t" , firstname:"Tricia", lastname:"Campbell"}
				]`
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "invalid credentials" }`
	
  * **Code:** 400 BAD REQUEST <br />
    **Content:** `{ error : "bad or missing parameter" }`

* **Sample Call:**

  `curl -X GET -H "Accept: application/json" "https://hostname/api/api/coursefriends?email=j@j.j&password=123456&coursename=101-916-DW&section=1"`
   
* **Notes:**

An empty array is returned if no friends found registered in the given course.