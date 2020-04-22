#MongoDB Cookbook

This cookbook install mongodb from source. It creates it's own apt package and then installs it. The recipe also create the config files and the service file with dynamic input of variables.

## list of what installs
- Mongodb

##Option and setting variables

Changes are made in the attribute file. Changing the port:
```
# attributes/default.rb

default['mongo']['port'] = <new_value_here>
```
##Commands

###test locally
Running my unit test:
```
chef exec rspec
```
running integration tests and closing machine:
```
kitchen test
```
##test in AWS

Running integration tests in AWS
```
KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
