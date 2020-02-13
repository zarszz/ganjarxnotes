---
layout: post
title: "Python requests module"
categories: tutorials
date: 2020-02-07
---

# Python3 Request Module 101

When fetch data or do network programming with python, we can use <strong>requests</strong> module for handling http request, because it's easy and flexible to use

-------------------------------

#### <span style="color: red">Official Documentation</span>
[python requests module](https://requests.readthedocs.io/en/master/)

------------------------------

## 1. Import Request Module
To ensure if requests module is avaible in our systems.<br/>

<strong>But, usually python is have requests module by default, so we can just import the module without install anything</strong>
```python
>>> import requests
```

## 2. GET request
To get data from somewhere
```python
>>> import requests
>>> request_result = requests.get('http://YOUR_TARGET')
```
Then, to change <strong>requests</strong> object result, we can use several function in requests module, in this example we will change request result object to [JSON](https://www.json.org/json-en.html)

```python
>>> request_json_result = request_result.json()
```
