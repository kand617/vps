# Getting started

## How to Build


The generated code has dependencies over external libraries like UniRest. These dependencies are defined in the ```PodFile``` file that comes with the SDK. 
To resolve these dependencies, we use the Cocoapods package manager.
Visit https://guides.cocoapods.org/using/getting-started.html to setup Cocoapods on your system.
Open command prompt and type ```pod --version```. This should display the current version of Cocoapods installed if the installation was successful.

Using command line, navigate to the directory containing the generated files (including ```PodFile```) for the SDK. 
Run the command ```pod install```. This should install all the required dependencies and create the ```pods``` directory in your project directory.

![Installing dependencies using Cocoapods](https://apidocs.io/illustration/objc?step=AddDependencies&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

Open the project workspace using the (SwaggerPetstore.xcworkspace) file. Invoke the build process using `Command(⌘)+B` shortcut key or using the `Build` menu as shown below.

![Building SDK using Xcode](https://apidocs.io/illustration/objc?step=BuildSDK&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)


## How to Use

The generated code is a Cocoa Touch Static Library which can be used in any iOS project. The support for these generated libraries go all the way back to iOS 6.

The following section explains how to use the SwaggerPetstore library in a new iOS project.     
### 1. Starting a new project
To start a new project, left-click on the ```Create a new Xcode project```.
![Create Test Project - Step 1](https://apidocs.io/illustration/objc?step=Test1&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

Next, choose **Single View Application** and click ```Next```.
![Create Test Project - Step 2](https://apidocs.io/illustration/objc?step=Test2&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

Provide **Test-Project** as the product name click ```Next```.
![Create Test Project - Step 3](https://apidocs.io/illustration/objc?step=Test3&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

Choose the desired location of your project folder and click ```Create```.
![Create Test Project - Step 4](https://apidocs.io/illustration/objc?step=Test4&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

### 2. Adding the static library dependency
To add this dependency open a terminal and navigate to your project folder. Next, input ```pod init``` and press enter.
![Add dependency - Step 1](https://apidocs.io/illustration/objc?step=Add0&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

Next, open the newly created ```PodFile``` in your favourite text editor. Add the following line : pod 'SwaggerPetstore', :path => 'Vendor/SwaggerPetstore'
![Add dependency - Step 2](https://apidocs.io/illustration/objc?step=Add1&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)

Execute `pod install` from terminal to install the dependecy in your project. This would add the dependency to the newly created test project.
![Add dependency - Step 3](https://apidocs.io/illustration/objc?step=Add2&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)


## How to Test

Unit tests in this SDK can be run using Xcode. 

First build the SDK as shown in the steps above and naivgate to the project directory and open the SwaggerPetstore.xcworkspace file.

Go to the test explorer in Xcode as shown in the picture below and click on `run tests` from the menu. 
![Run tests](https://apidocs.io/illustration/objc?step=RunTests&workspaceFolder=Swagger%20Petstore-ObjC&workspaceName=SwaggerPetstore&projectName=SwaggerPetstore&rootNamespace=SwaggerPetstore)


## Initialization

### 

Configuration variables can be set as following.
```Objc

```

# Class Reference

## <a name="list_of_controllers"></a>List of Controllers

* [PetsController](#pets_controller)

## <a name="pets_controller"></a>![Class: ](https://apidocs.io/img/class.png ".PetsController") PetsController

### Get singleton instance
```objc
Pets* pets = [[Pets alloc]init] ;
```

### <a name="list_pets_async_with_limit"></a>![Method: ](https://apidocs.io/img/method.png ".PetsController.listPetsAsyncWithLimit") listPetsAsyncWithLimit

> *Tags:*  ``` Skips Authentication ``` 

> List all pets


```objc
function listPetsAsyncWithLimit:(NSNumber*) limit
                completionBlock:(CompletedGetListPets) onCompleted(limit)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| limit |  ``` Optional ```  | How many items to return at one time (max 100) |





#### Example Usage

```objc
    // Parameters for the API call
    NSNumber* limit = 212;

    [self.pets listPetsAsyncWithLimit: limit  completionBlock:^(BOOL success, HttpContext* context, NSArray<Pet> * response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="create_pets_with_completion_block"></a>![Method: ](https://apidocs.io/img/method.png ".PetsController.createPetsWithCompletionBlock") createPetsWithCompletionBlock

> *Tags:*  ``` Skips Authentication ``` 

> Create a pet


```objc
function createPetsWithCompletionBlock:(CompletedPostCreatePets) onCompleted()
```



#### Example Usage

```objc

    [self.pets createPetsWithCompletionBlock:  ^(BOOL success, HttpContext* context, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



### <a name="get_show_pet_by_id_async_with_pet_id"></a>![Method: ](https://apidocs.io/img/method.png ".PetsController.getShowPetByIdAsyncWithPetId") getShowPetByIdAsyncWithPetId

> *Tags:*  ``` Skips Authentication ``` 

> Info for a specific pet


```objc
function getShowPetByIdAsyncWithPetId:(NSString*) petId
                completionBlock:(CompletedGetShowPetById) onCompleted(petId)
```

#### Parameters

| Parameter | Tags | Description |
|-----------|------|-------------|
| petId |  ``` Required ```  | The id of the pet to retrieve |





#### Example Usage

```objc
    // Parameters for the API call
    NSString* petId = @"petId";

    [self.pets getShowPetByIdAsyncWithPetId: petId  completionBlock:^(BOOL success, HttpContext* context, NSArray<Pet> * response, NSError* error) { 
       //Add code here
    }];
```

#### Errors

| Error Code | Error Description |
|------------|-------------------|
| 0 | unexpected error |



[Back to List of Controllers](#list_of_controllers)



