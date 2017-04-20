# Errors

<aside class="notice">FreshTEmp uses conventional HTTP response codes to indicate the success or failure of an API request. In general, codes in the 2xx range indicate success, codes in the 4xx range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a query failed, etc.), and codes in the 5xx range indicate an error with FreshTemps servers (not common).</aside>

The FreshTemp  API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request
401 | Unauthorized -- Your API key is wrong
403 | Forbidden -- You do not have access to this data
404 | Not Found -- The specified endpoint could not be found
405 | Method Not Allowed -- You tried to access an endpoint with an invalid method
406 | Not Acceptable -- You requested a format that isn't json
410 | Gone -- The endpoint requested has been removed.
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
