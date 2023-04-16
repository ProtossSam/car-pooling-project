# car-pooling-project

## Frontend:
We implement the frontend with code in HTML for page main structures, CSS for styling and JavaScript for some functions such as API requests and cookies operations.
There are below pages created:
1. index.html: the start page with login and register button
2. register.html: call the register API to stoer the user info in user-info tab
3. login.html: call the login API to get user info and store in cookie
4. select.html: ask the user to share a ride or look for a ride
5. profile.html: show the user info stored in the cookies
6. add_driver.html: call the add_driver API to store driver's availability in active-driver tab
7. find_driver.html" call the matching algo API to find the nearest driver

## Backend:
The backend logics are implemented with Python in AWS Lambda, then the functions are integrated with API Gateway to provide a REST API to be called by frontend.There are below APIs implemented:
1. user and driver related APIs: these APIs interact with the db for user and active drivers info
2. matching algo API: this API matches the rider with a list of active drivers and returns the nearest driver's info to the rider
3. notification API: this API informs the driver of the ride by SMS after it's matched

We also use DynamoDB to store the data of registered users and active drivers, two tables are created, user-info and active-driver.

## Deployment
We use AWS Amplify to host our web app.

