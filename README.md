# README
This is a place where features are managed across all Storyous systems. Purpose of this repository is to provide a convenient, easy to use and one standard way how to turn on/off separate features only for some merchants, tariffs, environments, versions of POS and so on. This repository is used as a configuration for our _features service_ application, which works as provider of features evaluation for all our other systems.

> As an online editor you can use [JSON Editor Online](http://www.jsoneditoronline.org/).

This repository consists of two main files at the moment of writing this readme file.

- features.json
- tariffs.json

## features.json
This is main configuration file. All the features goes there. Every feature in JSON is an array of string values.

### Usage examples:

#### environment:
- ```feature: ["test", "pre"]```
- Applies only for test and pre environment.

#### merchantId:
- ```feature: ["5315eb206c14b390ac60331e"]```
- Applies for specific merchant by it's merchantId.

#### tariff group:
- ```feature: ["tariff:profi,standard"]```
- Applies for tariffs in groups profi and standard as set in _tariffs.json_ file.

#### tariffId:
- ```feature: ["tariffId:553a61b39bfb20160000000b"]```
- Applies only for specified tariffs by it's tariffId.

#### list of merchantIds:
- ```feature: ["merchantId:55af5394e58fd6480000016e,55af5394e58fd64800000004"]```
- Applies for list of merchantIds.

#### POS version:
- ```feature: ["pos>=4.130"]```
- Applies for version of POS greater and equal to 4.130.
- **List of comparators which may also be used:**
    - ```feature: ["pos>=4.130"]``` - is greater and equal to
    - ```feature: ["pos=4.130"]``` - is onyl equal to
    - ```feature: ["pos<=4.130"]``` - is lesser and equal to
    - ```feature: ["pos>4.130"]``` - is greater than
    - ```feature: ["pos<4.130"]``` - is lesser than

## tariffs.json
Lists of tariffs separated logically into groups.
