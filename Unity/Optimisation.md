## SCRIPTABLE OBJECTS

A ScriptableObject is a data container that you can use to save large amounts of data, independent of class instances. 
One of the main use cases for ScriptableObjects is to reduce your Project’s memory usage by avoiding copies of values. 
This is useful if your Project has a Prefab that stores unchanging data in attached MonoBehaviour scripts .
Every time you instantiate that Prefab, it will get its own copy of that data. 
Instead of using the method, and storing duplicated data, you can use a ScriptableObject to store the data and then access it by reference from all of the Prefabs. 
This means that there is one copy of the data in memory.

## ASSET BUNDLES

An AssetBundle is an archive file that contains platform-specific non-code Assets (such as Models, Textures, Prefabs, Audio clips, and even entire Scenes) that Unity can load at run time. 
AssetBundle archive. The AssetBundle archive is a container, like a folder, that holds additional files inside it. These additional files consist of two types:

**serialized file** - which contains your Assets broken out into their individual objects and written out to this single file.
**Resource files** -  which are chunks of binary data stored separately for certain Assets (Textures and audio) to allow Unity to efficiently load them from disk on another thread.
