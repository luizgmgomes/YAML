# YAML


## Basics
  - Basically YAML is a superset of JSON. So, any valid JSON file is also a valid YAML file. 
  - In YAML the quotation marks ("") are optional, as long as you use the correct indentation, you should be fine.
  - You can use one or two spaces to indent, but you have to keep it consistent, the system you read it correctly (but most common use is two spaces).
  - NEVER use tabs in YAML file


## KEY & VALUE
Following the example below, we have:

---   <- This is a separator and only necessary if you are creating multiple structures of YAML inside the same file
appVersion: V1    
Kind: Pod
<----------------- Where "V1" and "Pod" are Values and "appVersion" and "Kind" are Keys


## There are two main types of structures we need to know:
  * Lists
  * Maps





* Maps

---
apiVersion: v1
kind: Pod
metadata:
  name: rss-site
  labels:
    app: web
    
In this case, we have a key, metadata, that has as its value a map with 2 more keys, name and labels. The labels key itself has a map as its value. 


















  
Source: https://www.mirantis.com/blog/introduction-to-yaml-creating-a-kubernetes-deployment/
