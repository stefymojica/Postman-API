# Bootcamp-API

## What will we do?

Using the following API definition https://petstore.swagger.io/#/ test it to verify that the information is saved correctly


## What was tested?

- POST: General tests to create a pet with different properties
- GET: Get the saved pet

## Note

- Some behaviors were found that were also automated:
    - **Id boolean**
        - When a POST is performed and a boolean value is passed in the id parameter, a 500 error is received
        - When getting a GET with a boolean id a 404 error is received
    - **Id negative number**
        - When a POST is made with a negative Id, the pet is created with a random id
        - When I GET a pet with a negative id I get a 404 error


## Dependencies


### Install Node.js

```
(> v16)
```

### Install newman

```
npm install -g newman
```

### Install HTML extra

```
npm i -g newman-reporter-htmlextra
```

## How to run the project

```
newman run Bootcamp-API.postman_collection.json
```


# How to run HTMl report

```
newman run Bootcamp-API.postman_collection.json -r htmlextra
```

2. Open HTML file in browser





