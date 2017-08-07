# 



## Base URL

The Base URL for this API is `http://petstore.swagger.io/v1`






# <a name="api_reference"></a>API Reference

* [pets](#pets)

## <a name="pets"></a>![Endpoint Group: ](https://apidocs.io/img/class.png "pets") pets


### <a name="list_pets"></a>![Endpoint: ](https://apidocs.io/img/method.png "listPets") listPets


**`GET`** `/pets`

> *Tags:*  ``` Skips Authentication ``` 

> List all pets



#### Query Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| limit | `number` |  ``` Optional ```  | How many items to return at one time (max 100) | `98` | 

#### Responses
**200** 

> An paged array of pets
Body (_Pet_) 
```
[
  {
    "id": "98",
    "name": "name",
    "tag": "tag"
  }
]
```


**Default** 

> unexpected error
Body (_Error_Error_) 
```
{
  "code": 98,
  "message": "message"
}
```


### <a name="create_pets"></a>![Endpoint: ](https://apidocs.io/img/method.png "createPets") createPets


**`POST`** `/pets`

> *Tags:*  ``` Skips Authentication ``` 

> Create a pet



#### Responses
**200** 

> Null response


**Default** 

> unexpected error
Body (_Error_Error_) 
```
{
  "code": 98,
  "message": "message"
}
```


### <a name="show_pet_by_id"></a>![Endpoint: ](https://apidocs.io/img/method.png "showPetById") showPetById


**`GET`** `/pets/{petId}`

> *Tags:*  ``` Skips Authentication ``` 

> Info for a specific pet



#### Path Parameters
| Parameter | Type | Tags | Description | Example |
|-----------|------| ---- |-------------| ------- |
| petId | `string` |  ``` Required ```  | The id of the pet to retrieve | `"petId"` | 

#### Responses
**200** 

> Expected response to a valid request
Body (_Pet_) 
```
[
  {
    "id": "98",
    "name": "name",
    "tag": "tag"
  }
]
```


**Default** 

> unexpected error
Body (_Error_Error_) 
```
{
  "code": 98,
  "message": "message"
}
```


[Back to API Reference](#api_reference)

