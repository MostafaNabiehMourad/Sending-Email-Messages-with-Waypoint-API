# Sending Email Messages with Waypoint API

This Python script demonstrates how to use the Waypoint API to send email messages. It utilizes the requests library to make an HTTP POST request to the Waypoint API endpoint. The script sends an email message based on a predefined template, with customizable variables such as the amount, refund ID, survey URL, and recipient's display name.

Code Explanation:

Import necessary libraries:

requests: Used to make HTTP requests.
json: Used to work with JSON data.
Define the API credentials:

API_KEY_USERNAME: Your API key username.
API_KEY_PASSWORD: Your API key password.
Specify the API endpoint URL:

url: The URL for the Waypoint API's email_messages endpoint.
Set the headers for the HTTP request:

headers: The headers include the content type, which is set to JSON.
Create authentication credentials:

auth: A tuple containing the API key username and password. These credentials are used for basic HTTP authentication.
Prepare the email message data:

data: A dictionary containing the following:
templateId: The ID of the email template to be used.
to: The recipient's email address.
variables: A dictionary of customizable variables for the email template, such as the amount, refund ID, survey URL, and recipient's display name.
Make an HTTP POST request to the Waypoint API:

response: Sends the POST request with the specified URL, headers, authentication credentials, and JSON data. The response object contains the result of the API call.
Check the response status code:

If the status code is 200, it indicates a successful email send operation.
If the status code is different from 200, it indicates a failure, and the script prints the status code and response content for debugging.
Usage:
To use this script, you need to replace the API_KEY_USERNAME, API_KEY_PASSWORD, to, and templateId with your specific API credentials and email template information. Customize the variables in the variables dictionary to match the content of your email.

Note:
Ensure that you have the requests library installed in your Python environment before running the script. You can install it using pip install requests.
