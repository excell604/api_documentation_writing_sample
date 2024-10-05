## API Documentation : OpenWeather API 
-> Welcome to the OpenWeather API documentation repository. This project is a part of my portfolio for demonstrating proficiency in API documentation using tools
   like Swagger, Postman, and GitHub.

The OpenWeather API provides access to real-time weather data for any city worldwide, which can be integrated into various applications, from mobile apps to data analytics platforms.

## Tools and Technologies
   - **Swagger**: Used for creating the API documentation.
   - **Postman**: For testing and demonstrating sample API calls.
   - **GitHub Wiki**: Contains detailed API documentation.

## API Endpoints Overview
    | HTTP Method | Endpoint                     | Description                        |
    |-------------|------------------------------|------------------------------------|
    | GET         | 'weather?q={city}&appid={key}'| Retrieve weather data for a city |

   city: name of city (required)
   key:  Your API key (required)

## How to Use the API

1. **Get your API Key**:
    - Sign up at [OpenWeather](https://home.openweathermap.org/users/sign_up) to obtain your API key.
  
2. **Make API Requests**:
    - Example request:
    GET https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY

## How to Authenticate

1.	Get Your API Key:
	  -After signing up, navigate to the API Keys section of your account and copy your unique key.
2.	Including Your API Key in Requests:
	  -You need to pass your API key as a query parameter in every request.
	  -The parameter is appid.
    Your API key should be kept private and not exposed in public repositories.

3. **Sample Response**;


   '''json

   `{`
   
    `"coord": {`
        `"lon": -0.1257,`
       ` "lat": 51.5085`
   
    `},`
   
   ` "weather": [
        {
            "id": 803,
            "main": "Clouds",
            "description": "broken clouds",
            "icon": "04n"
        }
    ],`
    // More fields....
     }

## Viewing Swagger Documentation Locally
1. Clone the repo:

Users should clone your repository containing the documentation files (e.g., swagger.yaml, server.js):

`git clone https://github.com/excell604/swagger-ui-docs.git`

2. Install Node.js and Dependencies

Ensure users have Node.js installed on their system. If they don’t, they can download it [here](https://nodejs.org/en).

Once Node.js is installed, navigate to the cloned repository and install the required dependencies by running:

`cd swagger-ui-docs
npm install`

This command will install any required modules such as express, swagger-ui-express, and yamljs.


3. Start the Server

After the dependencies are installed, users can start the local server using the following command:

`node server.js`

## Postman Collection

You can find the sample Postman collection [here](https://api.openweathermap.org/data/2.5/weather?q=London&appid=6cb2448603181bcb3ad20d85b05835b1)) to test the API requests yourself.

This will start the server, and users can access the Swagger UI documentation locally at: `http://localhost:3000/api-docs`

## Error handling

If you don’t include the correct API key, you will receive a 401 Unauthorized error:

`{
  "cod": 401,
  "message": "Invalid API key. Please see http://openweathermap.org/faq#error401 for more info."
}`

If you don’t type city names right, you will receive a 404 not found error:

`{
  "cod": "404",
  "message": "city not found"
}`
