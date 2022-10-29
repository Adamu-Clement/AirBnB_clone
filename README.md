
![App Screenshot](https://user-images.githubusercontent.com/37265965/198844664-d1af124e-c961-49c0-8b69-92c84e3c7929.JPG)


# AirBnB Clone Project - Console 

The Console is the fitst part of the AirBnB project assigned to the second sprint for ALX SE students. It a clone of the AirBnB website and its content in backend and frontend.
The objective of this project is cover up the basics and fundamental topics of higher programming languages and its applicability in the deployment of webservers.
In this segment we will have the opportunity of creating a command line interpreter with the module ```cmd``` and respond to it.

# Table Content 

|File          |      Method               | Description
------------- | -------------------------- | --------------
|[consol.py]() |comman interpreter | The starting point of the console functionality
|              | ```quit```          | it terminates the console functionality
|              | ```help```          | it gives information about a command line
|              | ```<emptyline> ```  | it loop the console when the user presses enter 
|              | ```create```        | it create instance of the Basemodel and saves it to JSON File 
|              | ``` show ```        | it shows and prints the string representation of the instances created
|              | ```destroy```       | it delete an instance based on the class name and id
|              | ```update```        | it update an instance based on the class name and id by adding or updating an attribute
|              | ```precmd```        | fixes the command line to be interpretable for console
|              | ```prepare_dict```  | prepare a string to update an isntance using dictionaries 
|              | ```prepare_line ``` |prepare the string to return an interpretable
| [base_model.py]()| instanciator    | The Basemodel defines all common attributes/methods for other classes
|             | ```def __init__(self, *args, **kwargs)```|initialization of the Basemodel recieving commands line    
|             | ```def save(self)``` |  it saves new instances and updates attributes to JSON file 
|             | ```def save(self)``` |  it return a dictionary containing keys/values of an instance
|             | ```def __str__(self)```| it print the string representation of the Basemodel class
|[classes that inherit from BaseModel]()| ```uer.py```| it represent the user 
|             | ```amenity.py```     | it represent the amenity that the user requires
|             | ```city.py```        | The city to visit 
|             | ```place.py```       | The place to stay 
|             | ```review.py```      | The critic of the place
|             | ```state.py```       | The State of the city 
|[file_storage.py]()| File Storage   | It serializes instances to JSON file and deserializes JSON file to instances
|             | ```all```| it return a dictionary of instances and attributes 
|             | ```new```| it sets the object to a new instance and key into the dictionary
|             | ```save```| it serializes the JSON file to a dictionary 

# Tests 
You will be able to see the different tests emphasis on certain methods, e.g: Creation of dictionaries, installation, creation of classes and attributes, etc.

| File | Method| Desription 
|-----|-------|-----------
|[tests_console.py]()|Test for sonsole| Checks how well the instantiation works
|                    | ```test_base_prep8_conformance_console```| Test that we conform to PEP8
|                    | ```base_pep8_conformance_consoletest``` | Test that we conform to PEP8 of the test itself
|tests_base_model.py | Test for the BaseModel Instaniator      | Checks how well the instantiation works
|                    | ```test_base_pep8_conformance_model```  | Test that we conform to PEP8 
|                    |```base_pep8_conformance_basemodeltest```   | Test that we conform to PEP8 of the test itself
|                    | ```instances```                         | test instance creation
|                    | ```test_time_attributes```              | It test the attribute of test_time_attributes
|                    | ```test_id_assignment```                | It tests the id assignment 
|                    | ```test_to_dict```                      | Tests dictionary instance 
|                    | ```test__str__```                       | Tests the printing
|                    | ```test_save```                         | Tests the save instances
| [test_models/]()   |test for classes                         | These tests checks for the same actions but the different attributes, they tend to be the same 
|[tests_city.py]()   | test city                               | Tests Attr:name, state_id
|[tests_places.py]() | test place                              | tests attr: city_id, user_id, name, description, number_rooms, number_bathrooms, max_guest, price_by_night, latitute, longitude, amenity_ids
|[tests_state.py]()  | test state                              | test attri: name
|[tests_review.py]() |test review                              | tests attr: place_id, user_id, text
|[tests_user.py]()   | test user                               | tests attr: email, password, first_name, last_name 
|[test_file_storage.py]()| test for File Storage class            | This test will test the storage of info in JSON file
|                     | ```test_all_dict_returned```           | test the method all when returns dict 
|                     | ```test_file_storage_exist```          | Checks if Methods exists 
|                     | ```test_new```                         | test the method new at the creation of new object
|                     | ```test_user_saveStorage```            | Checks if the save function works
|                     | ```test save```                        | test that properly saves  objects to file.JSON
|                     | ```test_BaseModel_saveStorage```       | Checks if the save function works
|                     | ```test_base_pep8_conformance_file_storage```| Test that we conform to PEP8
|                     | ```test_base_pep8_conformance_fileto_test```| Test that we conform to PEP of the test itself
|                     | ```test_file_storage_docstrings```     | test test_file_storage_docstrings


## Examples
To start the console, execute the file console.py ```./console.py``` and then write the command line. press enter to run the command.
```
Ubuntu@;[AirBnB_clone]; ~$./console.py 
(hbnb) help

Documented commands (type help <topic>):
=======================================
EOF  all  create  destroy  help  quit  show  update

(hbnb) all mymodel
** class doesn't exist **
(hbnb) create BaseModel
2750042b-bd56-417a-abae-f27c10352036
(hbnb) all BaseModel
["[BaseModel] (2750042b-bd56-417a-abae-f27c10352036) {'created_at': datetime.datetime(2022, 10, 24, 14, 27, 25, 108889), 'updated_at': datetime.datetime(2022, 10, 30, 14, 27, 25, 108979), 'id': '2750042b-bd56-417a-abae-f27c10352036'}", "[BaseModel] (c59f04fc-e383-4347-bf11-c7e3ddfbc400) {'__class__': 'BaseModel', 'created_at': datetime.datetime(2022, 10, 29, 4, 1, 43, 637709), 'updated_at': datetime.datetime(2022, 10, 29, 4, 1, 43, 637811), 'id': 'c59f04fc-e383-4347-bf11-c7e3ddfbc400'}", "[BaseModel] (33fd6e27-6c3a-481c-a517-7244602a90db) {'first_name': 'Betty', '__class__': 'BaseModel', 'created_at': datetime.datetime(2022, 10, 29, 3, 59, 47, 707579), 'updated_at': datetime.datetime(2022, 10, 29, 4, 1, 10, 362353), 'id': '33fd6e27-6c3a-481c-a517-7244602a90db'}"]
```

Here you can evidence the execusion of the commands help, create and all. As you can see, a new instance is created and then shown as a directory.

```
(hbnb) show BaseModel
** instance id missing **
(hbnb) show BaseModel 2750042b-bd56-417a-abae-f27c10352036
[BaseModel] (2750042b-bd56-417a-abae-f27c10352036) {'created_at': datetime.datetime(2022, 10, 30, 14, 27, 25, 108889), 'updated_at': datetime.datetime(2022, 10, 30, 14, 27, 25, 108979), 'id': '2750042b-bd56-417a-abae-f27c10352036'}
```

Here we want to see an instance created, but for that we need the specific id to see that instance.

```
(hbnb) destroy BaseModel 2750042b-bd56-417a-abae-f27c10352036
(hbnb) show BaseModel 2750042b-bd56-417a-abae-f27c10352036
** no instance found **
```
Here we want to delete an instance. We must give the id and then enter, itwill delete that instance. 

## All instances by class name
In order to fix the command interpreter for understanding the line by class name, the precmd was implementted. Here are few examples.
1. at first we could write these command:
```
(hbnb) all BaseModel
["[BaseModel] (28713969-89ec-4992-9d1e-cacceba1dc40) {'created_at': datetime.datetime(2022, 10, 1, 19, 45, 52, 553729), 'id': '28713969-89ec-4992-9d1e-cacceba1dc40', 'updated_at': datetime.datetime(2022, 7, 1, 19, 45, 52, 553744), '__class__': 'BaseModel'}"]
```
2. Now we can also write these lines, to simulate the python functionality.

```
(hbnb) BaseModel.all()
["[BaseModel] (28713969-89ec-4992-9d1e-cacceba1dc40) {'created_at': datetime.datetime(2022, 10, 1, 19, 45, 52, 553729), 'id': '28713969-89ec-4992-9d1e-cacceba1dc40', 'updated_at': datetime.datetime(2022, 10, 1, 19, 45, 52, 553744), '__class__': 'BaseModel'}"]
```
3. As evidence, here the id is given, therefore, will search the class required. 
```
(hbnb) BaseModel.all(28713969-89ec-4992-9d1e-cacceba1dc40)
["[BaseModel] (28713969-89ec-4992-9d1e-cacceba1dc40) {'created_at': datetime.datetime(2022, 10, 1, 19, 45, 52, 553729), 'id': '28713969-89ec-4992-9d1e-cacceba1dc40', 'updated_at': datetime.datetime(2022, 10, 1, 19, 45, 52, 553744), '__class__': 'BaseModel'}"]
```
4. We can also check how many times a class is  created as shown next: 
```
(hbnb) create User
3f649136-e3ca-4647-8c70-7ea448d954ce
(hbnb) create User
d23f5b6c-a3e7-4e01-942b-7a51056df50d
(hbnb) User.count()
2
(hbnb)
```
## Built with: 
1. Ubuntu 20.04 LTS
2.  Python3 (Version 3.8.5)



