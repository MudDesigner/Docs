Understanding the architecture
------------------------------

The Mud Engine is being developed to be extremely flexible. The goal of the project was to allow any developer to swap out any component within the engine, without needing to open up the the engine source code.

In order to achieve this, there were a few design choices made that all Mud developers using the engine should be aware of.

Mud Engine Core
***************

The core of the engine contains very little implementation logic. The idea behind the core is to provide a series of Types that would almost never be replaced. The rest of the content in the Core represents interfaces for other libraries to implement the details of.

An example of Types that would almost never be replaced would be the Mediator Types, some Exception and Argument Types along with some abstract base classes.

The core supports two different component types at runtime.

* Game components
* Adapters

A different project may implement the interfaces required by the engine as components, allowing different projects to have different sets of rules and behaviors. Components make up things that run in parallel with other objects in the game, but typically always on the engines main thread. An example of this would be characters, equipment and rooms.

A project may also adopt the Adapter system of the engine. Adapters can run on their own background thread if they want. Adapters allow a project to add complete new systems to the game, that were not originally accounted for by the engine. An example of this would be the world time, a networked server and complex persistance systems.

Mud Engine Game
***************