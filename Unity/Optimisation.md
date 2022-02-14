## SCRIPTABLE OBJECTS

A ScriptableObject is a data container that you can use to save large amounts of data, independent of class instances. 
One of the main use cases for ScriptableObjects is to reduce your Project’s memory usage by avoiding copies of values. 
This is useful if your Project has a Prefab that stores unchanging data in attached MonoBehaviour scripts .
Every time you instantiate that Prefab, it will get its own copy of that data. 
Instead of using the method, and storing duplicated data, you can use a ScriptableObject to store the data and then access it by reference from all of the Prefabs. 
This means that there is one copy of the data in memory.

## ASSET BUNDLES

An AssetBundle is an archive file that contains platform-specific non-code Assets (such as Models, Textures, Prefabs, Audio clips, and even entire Scenes) that Unity can load at run time.  When you make an asset "Addressable," you can use that asset's address to load it from anywhere.
AssetBundle archive. The AssetBundle archive is a container, like a folder, that holds additional files inside it. These additional files consist of two types:

**serialized file** - which contains your Assets broken out into their individual objects and written out to this single file.

**Resource files** -  which are chunks of binary data stored separately for certain Assets (Textures and audio) to allow Unity to efficiently load them from disk on another thread.


## ADDRESSABLES

The Addressables system provides tools and scripts to organize and package content for your application and an API to load and release assets at runtime. 
Flexibility, Dependancy Management, Memory management and Content Packing.

**How to initialise Addresables?** -   
Window > Package Manager  > Unity Registary > Addressables.
Window > Asset Management > Addressables > Groups

**Remote content distribution**
 - Content Delivery Network (CDN) or 
 - Unity's Cloud Content Delivery (CCD)

## CONTINUOUS INTEGRATION AND CONTINUOUS DEPLOYMENT (CICD)
 - **Continuous integration** is a step in which all code is merged as developers complete code in order to run automated builds and tests. 
 - **Continuous deployment** is the process of moving software that has been built and tested successfully into production.
 - Example - GIT

## SOLID PRINCIPLES

### SINGLE RESPONSIBILITY PRINCIPLE
Code we write should only be responsible for one specific task.

### OPEN-CLOSE PRINCIPLE
This principle stands for the rule of creating new behavior by extending existing classes instead of modifying the classes' source code. Therefore open for extension and closed for modification.

### LISKOV SUBSTITUTION PRINCIPLE
The Liskov Substitution Principle (LSP) states that child class objects should be able to replace parent-class objects without compromising the application's integrity. In other words, put effort into the creation of derived class objects which can replace objects of the base class without modifying its behavior. If we don’t do it that way, inheritance might break our application integrity.

### INTERFACE SEGREGATION PRINCIPLE
if a class needs to implement an interface it will take advantage of every function it needs to declare, if there are functions that not all classes need, then the interface should be divided in two or more interfaces.

### DEPENDANCY INVERSION PRINCIPLE
A High level modules should not depend upon low level modules. Both should depend upon abstractions.

