## DELEGATES

Delegate is a container for a function that can be used as a variable. Delegate helps in making code modular and efficient.
It works like a subscription-based service, where the passed method gets called when subscribed and vice versa.

There are two types of Delegates:

**Single-Cast Delegate — can hold single method.**

//Defining Delegate
public delegate void MyDelegate();
public static MyDelegate myDelegate;

//Subscribing to Single-Cast delegate
myDelegate = myMethod;

**Multi-Cast Delegate — can hold multiple methods**

//Subscribing to Multi-Cast delegate
myDelegate += myMethodOne;
myDelegate += myMethodTwo;

De-Assign method from delegate. To De-Assign methods from delegate, “-=” is used.
//UnSubscribing to Delegate
myDelegate -= myMethod;
myDelegate -=myMethodOne
myDelegate -=myMethodTwo
