# Getting started

## How to Build

The generated code uses a few Gradle dependencies e.g., Jackson, Volley,
and Apache HttpClient. The reference to these dependencies is already
added in the build.gradle file will be installed automatically. Therefore,
you will need internet access for a successful build.

* In order to open the client library in Android Studio click on ``` Open an Existing Android Project ```.

![Importing SDK into Android Studio - Step 1](https://apidocs.io/illustration/android?step=import1&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

* Browse to locate the folder containing the source code. Select the location of the SwaggerPetstore gradle project and click ``` Ok ```.

![Importing SDK into Android Studio - Step 2](https://apidocs.io/illustration/android?step=import2&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

* Upon successful import, the project can be built by clicking on ``` Build > Make Project ``` or  pressing ``` Ctrl + F9 ```.

![Importing SDK into Android Studio - Step 3](https://apidocs.io/illustration/android?step=import3&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

## How to Use

The following section explains how to use the SwaggerPetstore library in a new project.

### 1. Starting a new project 

For starting a new project, click on ``` Create New Android Studio Project ```.

![Add a new project in Android Studio - Step 1](https://apidocs.io/illustration/android?step=createNewProject0&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Here, configure the new project by adding the name, domain and location of the sample application followed by clicking ``` Next ```.

![Create a new Android Studio Project - Step 2](https://apidocs.io/illustration/android?step=createNewProject1&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Following this, select the ``` Phone and Tablet ```` option as shown in the illustration below and click ``` Next ```. 

![Create a new Android Studio Project - Step 3](https://apidocs.io/illustration/android?step=createNewProject2&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

In the following step, choose ``` Empty Activity ``` as the activity type and click ``` Next ```.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject3&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

In this step, provide an ``` Activity Name ``` and ``` Layout Name ``` and click ``` Finish ```.  This would take you to the newly created project.

![Create a new Android Studio Project - Step 4](https://apidocs.io/illustration/android?step=createNewProject4&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

### 2. Add reference of the library project

In order to add a dependency to this sample application, click on the android button shown in the project explorer on the left side as shown in the picture. Click on ``` Project ``` in the drop down that emerges.  

![Adding dependency to the client library - Step 1](https://apidocs.io/illustration/android?step=testProject0&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Right click the sample application in the project explorer and click on ``` New > Module ```  as shown in the picture.

![Adding dependency to the client library - Step 2](https://apidocs.io/illustration/android?step=testProject1&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Choose ``` Import Gradle Project ``` and click ``` Next ```.

![Adding dependency to the client library - Step 3](https://apidocs.io/illustration/android?step=testProject2&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Click on ``` Finish ``` which would take you back to the sample application with the refernced SDK. 

![Adding dependency to the client library - Step 4](https://apidocs.io/illustration/android?step=testProject3&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

In the following step naigate to the ``` SampleApplication >  app > build.gradle ``` file and add the following line ```compile project(path: ':SwaggerPetstore')``` to the dependencies section as shown in the illustration below.

![Adding dependency to the client library - Step 5](https://apidocs.io/illustration/android?step=testProject4&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

Finally, press ``` Sync Now ``` in the warning visible as shown in the picture below.

![Adding dependency to the client library - Step 6](https://apidocs.io/illustration/android?step=testProject5&workspaceFolder=Swagger%20Petstore&workspaceName=SwaggerPetstore&projectName=SwaggerPetstoreLib&rootNamespace=io.swagger.petstore)

### 3. Write sample code

Once the ``` SampleApplication ``` is created, a file named ``` SampleApplication > app > src > main > java > MainActivity ``` will be visible in the *Project Explorer* with an ``` onCreate ``` method. This is the entry point for the execution of the created project.
Here, you can add code to initialize the client library and instantiate a *Controller* class. Sample code to initialize the client library and using controller methods is given in the subsequent sections.

## How to Test

The generated code and the server can be tested using automatically generated test cases. 
JUnit is used as the testing framework and test runner.

In Android Studio, for running the tests do the following:

1. Right click on *SampleApplication > SwaggerPetstoreLib > androidTest > java)* from the project explorer.
2. Select "Run All Tests" or use "Ctrl + Shift + F10" to run the Tests.

## Initialization

### 

API client can be initialized as following. The `appContext` being passed is the Android application [`Context`](https://developer.android.com/reference/android/content/Context.html).

```java

io.swagger.petstore.Configuration.initialize(appContext);
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



