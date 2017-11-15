**Get all friends**
----
  Fetch all friends of the user (with authentication credentials email and password).

* **URL**

  /api/api/allfriends

* **Method:**
  
  `GET` 
  
*  **URL Params**

   **Required:**
 
   `email=[string]`
   `password=[string]`

* **Success Response:**

  * **Code:** 200 <br />
    **Content:** `[{email : "j@j.j" , firstname:"Jaya", lastname:"Nila"} ,
					{email : "t@t.t" , firstname:"Tricia", lastname:"Campbell"}
				]`
 
* **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "invalid credentials" }`

* **Sample Call:**

  `curl -X GET -H "Accept: application/json" "https://hostname/api/api/allfriends?email=j@j.j&password=123456"`
   
* **Notes:**

An empty array is returned if no friends found *sob*