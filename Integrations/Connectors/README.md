
# Connectors

A set of custom connectors created for Google SecOps Community to power up automation capabilities.

Python Version - V3_11


#### Dependencies
| |
|-|
|psycopg2_binary-2.9.10-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|setuptools-80.9.0-py3-none-any.whl|
|cronex-0.1.3.1.tar.gz|






## Connectors
#### Cron Scheduled Connector
A custom connector created to trigger playbooks by a given alert product, name and type and enables to edit the parameters according to your specific use case. 

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert fields|The alert fields you would like to insert in a json format|True|String|{
  "field_name_1": "field_value_1",
  "field_name_2": "field_value_2"
}|
|Alert name|The Alert name associated with the alert that will be created|True|String|<alert_name>|
|Alert type|The Alert type associated with the alert that will be created|False|String|<alert_type>|
|Cron Expression|If defined, will determine when the connector should create a case.|False|String||
|Product name|The Product name associated with the alert that will be created|False|String|<product_name>|


#### Scheduled Connector
A custom connector created to trigger playbooks by a given alert product, name and type and enables to edit the parameters according to your specific use case. 

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert fields|The alert fields you would like to insert in a json format|True|String|{
  "field_name_1": "field_value_1",
  "field_name_2": "field_value_2"
}|
|Alert name|The Alert name associated with the alert that will be created|True|String|<alert_name>|
|Alert type|The Alert type associated with the alert that will be created|False|String|<alert_type>|
|Product name|The Product name associated with the alert that will be created|False|String|<product_name>|




