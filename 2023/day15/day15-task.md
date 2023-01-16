# Task - day 15
- source code for desired outcomes as per task file
```
# Code for task 1
import json 

my_dict={
    "name":"John wick",
    "age":30,
    "city":"SanFransico"

}

with open("my_dict.json", "w") as json_file:
    json.dump(my_dict, json_file)

#code for task 2
print("This is code for task 2")

import json

# Opening the JSON file
with open("services.json", "r") as f:
    data = json.load(f)

# Getting  the keys of the services object
providers = data["services"].keys()

# Print the names of the service providers
for provider in providers:
    if provider == "debug":
        continue
    print(provider)


    #code for task 3
print("This is code for task 3")

import yaml
# Opening the YAML file
with open("services.yaml", "r") as yaml_file:
    # Loading the YAML data into a Python object
    yaml_data = yaml.safe_load(yaml_file)

# Converting the python object to JSON
json_data = json.dumps(yaml_data)

print(json_data)
```

- output: 

![Screenshot 2023-01-16 at 8 57 48 PM](https://user-images.githubusercontent.com/101057601/212713950-946ee17a-42f3-4330-b0a7-f62333a585a6.png)












