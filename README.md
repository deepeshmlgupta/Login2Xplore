
# Student Enrollment Form

It is a student registration form that stores the user's data in JSONPowerDB. It supports REST APIs and serverless technology. Students can be added, updated based on their roll number. In this form, the roll number is automatically checked and by the help of API, the data entered into other input fields sothat the user can update accordingly. The application uses AJAX requests for smooth and fast interaction. All kinds of data can be stored, such as numbers, strings, dates, etc.


## Benefits of using JsonPowerDB
- Can store structured / semi-structured and unstructured data along with other types of files and big-data.
- Dynamic relational constraints while using CRUD operations. i.e. Relational data can be managed without pre-defining PK, FK, UK, databases, tables etc.
- Free from technology constraints - Low-Code and easy to use from any technology via HTTP Rest API.
- Minimum learning curves, builds faster, cuts time to market, reduces the development cost.
- Helps developers in managing their databases using various tools and techniques.



# Release History

## JsonPowerDB

### Version: 2.0

#### Execute API

```javascript
var baseUrl = "http://api.login2explore.com:5577";
function executeCommand(reqString, apiEndPointUrl) {
    var url = baseUrl + apiEndPointUrl;
    var jsonObj;
    $.post(url, reqString, function (result) {
        jsonObj = JSON.parse(result);
    }).fail(function (result) {
        var dataJsonObj = result.responseText;
        jsonObj = JSON.parse(dataJsonObj);
    });
    return jsonObj;
}
```
## Create a PUT Request String

```javascript
function createPUTRequest(connToken, jsonObj, dbName, relName) {
    var putRequest = "{\n"
            + "\"token\" : \""
            + connToken
            + "\","
            + "\"dbName\": \""
            + dbName
            + "\",\n" + "\"cmd\" : \"PUT\",\n"
            + "\"rel\" : \""
            + relName + "\","
            + "\"jsonStr\": \n"
            + jsonObj
            + "\n"
            + "}";
    return putRequest;
}

```
## Features

- Simple to Use
- Fast Response
- Detailed User Interface


## Tech Stack

**Client:** HTML,CSS,Javascript

**Server:** JsonPowerDB
