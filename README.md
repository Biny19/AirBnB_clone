<!DOCTYPE html>
<html>
<head>
<style>
table, th, td {
  border: 1px solid black;
  border-collapse: collapse;
}
</style>
</head>
<body>
<h1>Description:</h1>
<p>
This team project is one part of the ALX SWE Full-Stack Software Engineer program. It's the first step towards building a first full web application, 
an AirBnB clone. First this project consists of a custom command-line interface for data management, and the base classes for the storage of this data.Console commands allow the user to create, update, and destroy objects, as well as manage file storage. Using a system of JSON serialization/deserialization,
storage is persistent between sessions.
</p>
<h1>Usage:</h1>
<p>
The console works both in interactive mode and non-interactive mode, much like a Unix shell. It prints a prompt (hbnb) and waits for the user for input.
</p>
<table style="width:100%" >
  <tr>
    <th>Command	</th>
    <th>Example</th>
  </tr>
  <tr>
    <td>Run the console	</td>
    <td>./console.py</td>
  </tr>
  <tr>
    <td>Quit the console</td>
    <td>(hbnb) quit</td>
  </tr>
    <tr>
    <td>Display the help for a command	</td>
    <td>(hbnb) help "command"</td>
  </tr>
    <tr>
    <td>Create an object (prints its id)</td>
    <td>(hbnb) create "class"</td>
  </tr>
    <tr>
    <td>Show an object</td>
    <td>(hbnb) show "class", id or (hbnb) class.show(<id>)</td>
  </tr>
    <tr>
    <td>Destroy an object</td>
    <td>(hbnb) destroy class, id or (hbnb) class.destroy(id)</td>
  </tr>
    <tr>
    <td>Show all objects, or all instances of a class	</td>
    <td>(hbnb) all or (hbnb) all class</td>
  </tr>
    <tr>
    <td>Update an attribute of an object</td>
    <td>(hbnb) update class, id, attribute name, attribute value or (hbnb) class.update(id, attribute name, attribute value)</td>
  </tr>
</table>
<pre>
Non-interactive mode example
$ echo "help" | ./console.py
(hbnb)
Documented commands (type help <topic>):
========================================
EOF  all  count  create  destroy  help  quit  show  update
</pre>
<h1>Models:</h1>
<p>The folder models contains all the classes used in this project.</p>
<table style="width:100%" >
  <tr>
    <th>File</th>
    <th>Description</th>
     <th>Attributes</th>
  </tr>
  <tr>
    <td>base_model.py 	</td>
    <td>BaseModel class for all the other classes</td>
    <td>id, created_at, updated_at</td>
  </tr>
  <tr>
    <td>user.py </td>
    <td>User class for future user information</td>
    <td>email, password, first_name, last_name</td>
  </tr>
    <tr>
    <td>amenity.py</td>
    <td>Amenity class for future amenity information</td>
    <td>name</td>
  </tr>
    <tr>
    <td>city.py	</td>
    <td>City class for future location information</td>
    <td>state_id, name</td>
  </tr>
    <tr>
    <td>state.py</td>
    <td>State class for future location information</td>
    <td>name</td>
  </tr>
    <tr>
    <td>place.py</td>
    <td>Place class for future accommodation information</td>
    <td>city_id, user_id, name, description,number_rooms, number_bathrooms, max_guest, price_by_night, latitude, longitude, amenity_ids</td>
  </tr>
    <tr>
    <td>review.py</td>
    <td>Review class for future user/host review information</td>
    <td>place_id, user_id, text</td>
  </tr>
</table>
<h1>File storage:</h1>
<pre>
The folder engine manages the serialization and deserialization of all the data, following a JSON format.
A FileStorage class is defined in file_storage.py with methods to follow this flow:
(object) -> to_dict() -> (dictionary) -> JSON dump -> (json string) -> FILE -> (json string) -> JSON load -> (dictionary) -> (object)
</pre>
<p>
The init.py file contains the instantiation of the FileStorage class called storage, followed by a call to the method reload() on that instance.
This allows the storage to be reloaded automatically at initialization, which recovers the serialized data.
</p>
<h1>Tests:</h1>
<p>
All the code is tested with the unittest module. The test for the classes are in the test_models folder.
</p>
</body>
</html>
