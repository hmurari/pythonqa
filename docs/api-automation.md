# Chapter 7: API Automation

## 7.1 Introduction to Web APIs

Application Programming Interfaces (APIs) are a crucial part of the modern web. They allow applications to communicate with each other and exchange information, making it easier for developers to build and integrate various services. Web APIs, specifically, provide a way for applications to interact with web services using standardized protocols like HTTP.

In this chapter, we will explore how to automate web APIs using Python. We will cover the following topics:

- Making API requests using the Requests library
- Handling JSON data in Python
- Project - Automating weather data retrieval using OpenWeatherMap API

By the end of this chapter, you will have a good understanding of how to work with web APIs and how to automate their usage in your Python projects.


## 7.2 Making API Requests using the Requests Library

Python's Requests library provides a simple and elegant way to interact with web APIs. It allows you to send HTTP/1.1 requests, handle responses, and easily integrate with web services.

To make a request using the Requests library, you first need to install it. You can do this using pip, the Python package manager, by running the following command:

``` bash
pip install requests
```

Once installed, you can import the library and start making requests. Here's an example of how to make a simple GET request:

``` python
import requests

response = requests.get('https://jsonplaceholder.typicode.com/posts')

print(response.status_code)
print(response.json())
```

!!! note
    In this example, we make a GET request to the `JSONPlaceholder` API, which returns a list of posts in JSON format. We then print the HTTP status code and the JSON data returned by the API.

Requests supports various HTTP methods like GET, POST, PUT, DELETE, and more. It also allows you to add parameters, headers, and other options to your requests. You can check out the Requests library documentation for more information and examples.

In the next section, we will discuss how to handle JSON data in Python.

## 7.3 Handling JSON Data in Python

JSON (JavaScript Object Notation) is a lightweight data format that is widely used in web APIs to transmit data between client and server. Python provides a built-in module called `json` to handle JSON data.

To work with JSON data in Python, you first need to import the `json` module. Here's an example of how to load JSON data from a string:

```python
import json

json_string = '{"name": "John", "age": 30, "city": "New York"}'

data = json.loads(json_string)

print(data)
print(data['name'])
```

!!! note
    In this example, we load a `JSON` string into a Python dictionary using the `json.loads()` method. We then print the dictionary and access the value of the name key.
    
Similarly, you can use the `json.dumps()` method to convert a Python object into a JSON string:

``` python
import json

data = {
    'name': 'John',
    'age': 30,
    'city': 'New York'
}

json_string = json.dumps(data)

print(json_string)
```

In this example, we convert a Python dictionary into a JSON string using the `json.dumps()` method.

In the next section, we will apply what we have learned so far to automate weather data retrieval using the OpenWeatherMap API.


## 7.4 Project - Automating Weather Data Retrieval using OpenWeatherMap API

In this project, we will apply the concepts we have learned so far to automate the retrieval of weather data using the OpenWeatherMap API.

!!! API-Key
    Before we can use the OpenWeatherMap API, we need to obtain an API key. You can sign up for a free account at https://home.openweathermap.org/users/sign_up and obtain an API key from your account dashboard.

### 7.4.2 Making API Requests

Once you have obtained an API key, you can start making requests to the OpenWeatherMap API. Here's an example of how to retrieve the current weather data for a city using the Requests library:

```python
import requests
import json

api_key = '<your_api_key>'
city = 'New York'

url = f'https://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}'

response = requests.get(url)

data = json.loads(response.text)

print(f'Current temperature in {city}: {data["main"]["temp"]} K')
```

In this example, we retrieve the current weather data for London using the OpenWeatherMap API. We first construct the API URL with the API key and the desired city. We then make a GET request to the API using the Requests library and load the JSON response into a Python dictionary. Finally, we print the current temperature in the city.



### 7.4.3 Project Task


Your task is to write a Python script that automates the retrieval of weather data for a list of cities using the OpenWeatherMap API. The script should read the list of cities from a file and output the weather data to another file.


Here are the requirements for the project:

- The input file should contain a list of cities, one per line.
- The script should use the OpenWeatherMap API to retrieve the current weather data for each city.
- The script should output the weather data to a CSV file, with columns for city, temperature, humidity, pressure, and wind speed.
- The script should handle errors gracefully, such as when a city is not found or the API request fails.

You can use the examples and concepts discussed in this chapter to complete the project. Good luck!


## 7.5 Additional Resources

Here are some additional resources for learning about web APIs and Python:

- The Requests library documentation: https://docs.python-requests.org/en/master/
- The JSON module documentation: https://docs.python.org/3/library/json.html
- The OpenWeatherMap API documentation: https://openweathermap.org/api
- The Python API tutorial: https://realpython.com/python-api/
- The REST API tutorial: https://restfulapi.net/

In addition to these resources, there are many web APIs available for practicing and learning. You can explore APIs for social media platforms, e-commerce websites, news outlets, and more.

Remember to always read the API documentation carefully and follow any usage limits or restrictions. Happy automating!

## 7.6 Summary

In this chapter, we learned about web APIs and how to automate them using Python. We covered the basics of making API requests using the Requests library, and how to handle JSON data in Python. We also completed a project that demonstrated how to retrieve weather data using the OpenWeatherMap API.

API automation is a powerful tool for integrating different applications and services. By using web APIs, we can retrieve and manipulate data in a programmatic way, without the need for manual intervention. Python provides many libraries and tools for working with web APIs, making it an ideal language for API automation.

