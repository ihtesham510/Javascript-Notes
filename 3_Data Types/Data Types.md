# Overview
```mermaid
flowchart 
    id1{Data Types}===ide1[Primitive Types]
    id1{Data Types}===Object---id2[Object Prototype];
    id1{Data Types}===id5[typeof operator];
    id2[Object Prototype]---id3[Prototype Inheitence]
    
    subgraph ide1[Primitive Types]
     direction RL
      String---Boolean---Undefined---Bigint;
      String---Number---Symbol---Bigint;
    end
    Object===id4[Built in Objects]

```

# **Data Types**
In JavaScript and also other programming languages, there are different types of data types. The following are JavaScript primitive data types: _String, Number, Boolean, undefined, Null_, and _Symbol_.
# Primitive Types
## String
## Number
## Boolean
## Undefined
## Null
## Symbol
## Bigint