## PREFAB

**1. What is Prefab?**
Asset type that allows you to store a GameObject object complete with components and properties. The prefab acts as a template from which you can create new object instances in the scene. 
Any edits made to a prefab asset are immediately reflected in all instances produced from it but you can also override components and settings for each instance individually.

**2. What is Nested Prefab?**
Prefabs instances inside other Prefabs. This is called nesting Prefabs. 
Nested Prefabs retain their links to their own Prefab Assets, while also forming part of another Prefab Asset.

     - Instantiate another nested prefab by **PrefabUtility.InstantiatePrefab**
     - Modify that new GameObject of the prefab
     - Save the modification by **PrefabUtility.SaveAsPrefabAssetAndConnect**

## EXECUTIONS

**1. The order of execution**

     - Awake()
     - OnEnable()
     - Start()
     - FixedUpdate()
     - Update()
     - LateUpdate()
     - OnGUI()
     - OnApplicationQuit()
     - OnDisable()
     - OnDestroy()
     

**2. Awake()**

This function is always called before any Start functions and also just after a prefab is instantiated. 
(If a GameObject is inactive during start up Awake is not called until it is made active.)


**OnEnable()**

This function is called just after the object is enabled. 
This happens when a MonoBehaviour instance is created, such as when a level is loaded or a GameObject with the script component is instantiated.


**3. Start()**

Start is called before the first frame update only if the script instance is enabled.


**4. FixedUpdate()**

FixedUpdate is often called more frequently than Update. 
It can be called multiple times per frame, if the frame rate is low and it may not be called between frames at all if the frame rate is high. 
All physics calculations and updates occur immediately after FixedUpdate. 
When applying movement calculations inside FixedUpdate, you do not need to multiply your values by Time.deltaTime. 
This is because FixedUpdate is called on a reliable timer, independent of the frame rate.


**5. Update()**

Update is called once per frame. It is the main workhorse function for frame updates.


**6. LateUpdate()**

LateUpdate is called once per frame, after Update has finished. 
Any calculations that are performed in Update will have completed when LateUpdate begins. 
A common use for LateUpdate would be a following third-person camera. 
If you make your character move and turn inside Update, you can perform all camera movement and rotation calculations in LateUpdate. 
This will ensure that the character has moved completely before the camera tracks its position.


**7. OnGUI()**

OnGUI is called for rendering and handling GUI events. Graphics User Interface


**8. OnApplicationQuit()**

This function is called on all game objects before the application is quit. In the editor it is called when the user stops playmode.


**9. OnDisable()**

This function is called when the behaviour becomes disabled or inactive.


**10. OnDestroy()**

This function is called after all frame updates for the last frame of the object’s existence (the object might be destroyed in response to Object.Destroy or at the closure of a scene).

## TIME

https://docs.unity3d.com/ScriptReference/Time.html

**Delta Time** - The interval in seconds from the last frame to the current one

**Fixed Delta Time** - The interval in seconds at which physics and other fixed frame rate updates are performed.

**Fixed Time** - The time since the last FixedUpdate started.

**Frame Conut** - The total number of frames since the start of the game.

**Capture Delta Time** - Slows your application’s playback time to allow Unity to save screenshots in between frames.

**Smooth Delta Time** - A smoothed out Time.deltaTime

**Time.time** returns the amount of time since your project started playing.

**Time.deltaTime** returns the amount of time that elapsed since the last frame completed.

**Time.timeScale** represents the rate at which time elapses. You can read this value, or set it to control how fast time passes, allowing you to create slow-motion effects.

## RANDOM

**Random.value** gives you a random floating point number between 0.0 and 1.0.

**Random.Range** gives you a random number between a minimum and maximum value that you provide.

**Random.rotation** To generate a random rotation.

**Random.ColorHSV** To generate a random color.

