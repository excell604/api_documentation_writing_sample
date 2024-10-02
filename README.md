## API Documentation : Weather API 
-> Welcome to the OpenWeather API documentation repository. This project is a part of my portfolio for demonstrating proficiency in API documentation using tools
   like Swagger, Postman, and GitHub.
   The OpenWeather API allows users to retrieve current weather data for any city worldwide. The API is fully documented with examples of requests and responses, including authentication
   and usage details.

## Tools and Technologies
   - **Swagger**: Used for creating the API documentation.
   - **Postman**: For testing and demonstrating sample API calls.
   - **GitHub Wiki**: Contains detailed API documentation.

## API Endpoints Overview
    | HTTP Method | Endpoint                     | Description                        |
    |-------------|------------------------------|------------------------------------|
    | GET         | 'weather?q={city}&appid={key}'| Retrieve weather data for a city |

## How to Use the API

1. **Get your API Key**:
    - Sign up at [OpenWeather](https://home.openweathermap.org/users/sign_up) to obtain your API key.
  
2. **Make API Requests**:
    - Example request:
  GET https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY

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
2. Go to the Swagger folder and open the 'index.html' file in your browser to view the API documentation.

### Postman Collection

You can find the sample Postman collection [here](https://api.openweathermap.org/data/2.5/weather?q=London&appid=6cb2448603181bcb3ad20d85b05835b1)) to test the API requests yourself.

## Error handling
{
  "cod": 401,
  "message": "Invalid API key. Please see http://openweathermap.org/faq#error401 for more info."
}
