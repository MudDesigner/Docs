Setting up the Mud Engine on Windows
------------------------------------

.. include:: /shared/under-construction.txt

As the engine is still under development and doesn't have an official binary release yet, you can clone the repository, compile it and use it to create your games.

.. note::
    The engine is still under heavy development. There **will** be breaking changes.
	
You may visit the projects `GetHub Home Page <http://github.com/MudDesigner/Home/>`_ to see all of the available repositories you can clone. 

.. image:: /_static/github-home.PNG

To get up and running, you will need to clone the Mud Engine repository at a minimum, along with have Visual Studio 2015 Community Edition or greater installed. This will bring down the core engine components and a basic implementation of a game system. The Mud Engine repository does not include any servers.

.. image:: /_static/team-explorer.PNG

Once you have the repository cloned, you should see the repository available for you to view from within Visual Studio.

.. image:: /_static/cloned-repository.PNG

Opening the local Git repository will show you the Visual Studio solution file that you can open. If one does not exist, you can browse for one in the directory that the repository was cloned to. You will need to look for the *MudDesigner.MudEngine.sln* filename.

.. image:: /_static/repository-view.PNG

With the solution loaded, you should see all of the available projects associated with the Mud Engine solution.

.. image:: /_static/solution.PNG

Rebuild the solution, and then navigate to the /bin directory within the *MudEngine.Core* project. You will need to copy the .dll files out of there when you create your new project.

Next, you will need to create a new project in Visual Studio. Once you have one created, add the compiled Mud Engine assemblies to your project as a reference. You are now ready to start building your own game.