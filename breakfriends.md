**Get friends who are not in class at any point within the supplied period**
----
  Fetch all friends of the user (with authentication credentials email and password), who are not in a class at some point during the supplied period. The period is specified by day, start time and end time.

* **URL**

  /api/api/breakfriends

* **Method:**
  
  `GET` 
  
*  **URL Params**

   **Required:**
 
   `email=[string]`
   `password=[string]`
   `day=[integer]`
   `start=[integer]`
   `end=[integer]`

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

  `curl -X GET -H "Accept: application/json" "https://hostname/api/api/coursefriends?email=j@j.j&password=123456&day=1&start=1000&end=1300"`
   
* **Notes:**

An empty array is returned if no friends found having an overlapping break 