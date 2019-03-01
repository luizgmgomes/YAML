# **YAML**


## Basics
  - Basically YAML is a superset of JSON. So, any valid JSON file is also a valid YAML file. 
  - In YAML the quotation marks ("") are optional, as long as you use the correct indentation, you should be fine.
  - You can use one or two spaces to indent, but you have to keep it consistent, the system you read it correctly (but most common use is two spaces).
  - NEVER use tabs in YAML file


## KEY & VALUE

    ---   
    appVersion: V1    
    Kind: Pod

  * Following the example below, we have:
    * The three dashes act as separators and are only necessary if you are creating multiple structures of YAML inside the same file
    * **KEYS**: "appVersion" and "Kind"
    * **VALUES**: "V1" and "Pod" 
    
    
## There are two main types of structures we need to know:
  * Lists
  * Maps

### Maps

    ---
    apiVersion: v1
    kind: Pod
    metadata:
      name: rss-site
      labels:
        app: web
    
  * In this example, we have a **KEY**, metadata, that has as its value a **MAP** with 2 more **KEYS**, name and labels. The labels **KEY** itself is another **map** with a single a **KEY** (app) and **VALUE** (web).


### Lists
  
  * Also called "hash" or "dictionaries"

    ```args:
      - sleep
      - "1000"
      - message
      - "Bring back Firefly!"
    ```
  * You can basically have any number of items on the *LIST*, as long as they are indented from the parent and have a "hifen" at the beginning. 
  A comparison with JSON would be
  ```
  {
   "args": ["sleep", "1000", "message", "Bring back Firefly!"]
  }
  ```
  
  
      




















  
Source: https://www.mirantis.com/blog/introduction-to-yaml-creating-a-kubernetes-deployment/
