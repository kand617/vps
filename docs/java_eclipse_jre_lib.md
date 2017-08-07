# Getting started

## How to Build

The generated code uses a few Maven dependencies e.g., Jackson, UniRest,
and Apache HttpClient. The reference to these dependencies is already
added in the pom.xml file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Eclipse click on ``` File -> Import ```.

![Importing SDK into Eclipse - Step 1](https://apidocs.io/illustration/java?step=import0&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

* In the import dialog, select ``` Existing Java Project ``` and click ``` Next ```.

![Importing SDK into Eclipse - Step 2](https://apidocs.io/illustration/java?step=import1&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

* Browse to locate the folder containing the source code. Select the detected location of the project and click ``` Finish ```.

![Importing SDK into Eclipse - Step 3](https://apidocs.io/illustration/java?step=import2&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

* Upon successful import, the project will be automatically built by Eclipse after automatically resolving the dependencies.

![Importing SDK into Eclipse - Step 4](https://apidocs.io/illustration/java?step=import3&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

## How to Use

The following section explains how to use the SwaggerPetstore library in a new console project.

### 1. Starting a new project

For starting a new project, click the menu command ``` File > New > Project ```.

![Add a new project in Eclipse](https://apidocs.io/illustration/java?step=createNewProject0&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Next, choose ``` Maven > Maven Project ```and click ``` Next ```.

![Create a new Maven Project - Step 1](https://apidocs.io/illustration/java?step=createNewProject1&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Here, make sure to use the current workspace by choosing ``` Use default Workspace location ```, as shown in the picture below and click ``` Next ```.

![Create a new Maven Project - Step 2](https://apidocs.io/illustration/java?step=createNewProject2&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Following this, select the *quick start* project type to create a simple project with an existing class and a ``` main ``` method. To do this, choose ``` maven-archetype-quickstart ``` item from the list and click ``` Next ```.

![Create a new Maven Project - Step 3](https://apidocs.io/illustration/java?step=createNewProject3&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

In the last step, provide a ``` Group Id ``` and ``` Artifact Id ``` as shown in the picture below and click ``` Finish ```.

![Create a new Maven Project - Step 4](https://apidocs.io/illustration/java?step=createNewProject4&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

### 2. Add reference of the library project

The created Maven project manages its dependencies using its ``` pom.xml ``` file. In order to add a dependency on the *SwaggerPetstoreLib* client library, double click on the ``` pom.xml ``` file in the ``` Package Explorer ```. Opening the ``` pom.xml ``` file will render a graphical view on the cavas. Here, switch to the ``` Dependencies ``` tab and click the ``` Add ``` button as shown in the picture below.

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/java?step=testProject0&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Clicking the ``` Add ``` button will open a dialog where you need to specify SwaggerPetstore in ``` Group Id ``` and SwaggerPetstoreLib in the ``` Artifact Id ``` fields. Once added click ``` OK ```. Save the ``` pom.xml ``` file.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject1&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

### 3. Write sample code

Once the ``` SimpleConsoleApp ``` is created, a file named ``` App.java ``` will be visible in the *Package Explorer* with a ``` main ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/java?step=testProject2&workspaceFolder=Swagger%20Petstore-Java&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Eclipse, for running the tests do the following:

1. Select the project *SwaggerPetstoreLib* from the package explorer.
2. Select "Run -> Run as -> JUnit Test" or use "Alt + Shift + X" followed by "T" to run the Tests.

## Initialization

### 

API client can be initialized as following.

```java

SwaggerPetstoreClient client = new SwaggerPetstoreClient();
```


# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PetsController](#pets_controller)

## <a name="pets_controller"></a>![Class: ](https://apidocs.io/img/class.png "io.swagger.petstore.controllers.PetsController") PetsController

### Get singleton instance

The singleton instance of the ``` PetsController ``` class can be accessed from the API Client.

```java
PetsController pets = client.getPets();
```

### <a name="list_pets_async"></a>![Method: ](https://apidocs.io/img/method.png "io.swagger.petstore.controllers.PetsController.listPetsAsync") listPetsAsync

> *Tags:*  ``` Skips Authentication ``` 

> List all pets


```java
void listPetsAsync(
        final Integer limit,
        final APICallBack<List<Pet>> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| limit |  ``` Optional ```  | How many items to return at one time (max 100) |


#### Example Usage

```java
Integer limit = 98;
// Invoking the API call with sample inputs
pets.listPetsAsync(limit, new APICallBack<List<Pet>>() {
    public void onSuccess(HttpContext context, List<Pet> response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="create_pets_async"></a>![Method: ](https://apidocs.io/img/method.png "io.swagger.petstore.controllers.PetsController.createPetsAsync") createPetsAsync

> *Tags:*  ``` Skips Authentication ``` 

> Create a pet


```java
void createPetsAsync(final APICallBack<Object> callBack)
```

#### Example Usage

```java
// Invoking the API call with sample inputs
pets.createPetsAsync(new APICallBack<void>() {
    public void onSuccess(HttpContext context, void response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="get_show_pet_by_id_async"></a>![Method: ](https://apidocs.io/img/method.png "io.swagger.petstore.controllers.PetsController.getShowPetByIdAsync") getShowPetByIdAsync

> *Tags:*  ``` Skips Authentication ``` 

> Info for a specific pet


```java
void getShowPetByIdAsync(
        final String petId,
        final APICallBack<List<Pet>> callBack)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| petId |  ``` Required ```  | The id of the pet to retrieve |


#### Example Usage

```java
String petId = "petId";
// Invoking the API call with sample inputs
pets.getShowPetByIdAsync(petId, new APICallBack<List<Pet>>() {
    public void onSuccess(HttpContext context, List<Pet> response) {
        // TODO success callback handler
    }
    public void onFailure(HttpContext context, Throwable error) {
        // TODO failure callback handler
    }
});

```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



[Back to List of Controllers](#list_of_controllers)



