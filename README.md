# cat-facts-api-tests
This repository contains test cases for the Cat Facts API to ensure its functionality and reliability.

Test Cases Table
| Test Case ID | Description                              | Steps                                                                 | Expected Result                                                                                       | Validation Method                                                                                             |
|---------------|------------------------------------------|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| TC1           | Retrieve a Random Cat Fact               | 1. Send GET request to `https://catfact.ninja/fact`.<br>2. Capture response.             | 1. Status code 200.<br>2. JSON object with keys `fact` and `length`.                               | - Status Code Check<br>- JSON Validation<br>- Fact Validity<br>- Length Validity                              |
| TC2           | Retrieve Multiple Cat Facts               | 1. Send GET request to `https://catfact.ninja/facts`.<br>2. Capture response.            | 1. Status code 200.<br>2. JSON object with key `data` containing an array of cat facts.             | - Status Code Check<br>- JSON Validation<br>- Array Validation<br>- Element Validity                          |
| TC3           | Check for the `limit` Parameter          | 1. Send GET request to `https://catfact.ninja/facts?limit=5`.<br>2. Capture response.    | 1. Status code 200.<br>2. JSON object with key `data` containing an array of 5 elements.            | - Status Code Check<br>- JSON Validation<br>- Array Size Verification<br>- Element Validity                  |
| TC4           | Check for Invalid Request                 | 1. Send GET request to `https://catfact.ninja/facts?limit=abc`.<br>2. Capture response.  | 1. Status code 400 (or error code).<br>2. JSON object containing an error message.                  | - Status Code Check<br>- JSON Validation<br>- Error Message Verification                                      |

Validation Description

The validation methods used in these test cases focus on ensuring that the API responds correctly to both valid and invalid requests. By checking status codes, validating JSON structure, and verifying the content of responses, we can confirm that the API behaves as expected. This thorough approach helps ensure the API's reliability and usability for developers and users alike.
