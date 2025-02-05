# city-builder
city building game
files i am using to build my own game engine that i can use with the game that i am building. CityBuilder is the name of the game. is a city building game.

# here is what i have
Project Setup:

The project directory is located at C:\game_engine.
I am using CMake 3.31 and I am set up a CMakeLists.txt file for building a project.

# Libraries & Dependencies:
I am planning to use OpenGL for rendering and a custom physics engine for collision detection, rigid bodies, and gravity.
I am also focusing on input handling for keyboard, mouse, and gamepad support.

spdlog – A fast, header-only logging library.
EnTT – An Entity Component System (ECS) framework.
OpenGL – For rendering graphics.
GLFW – For window creation and input handling (keyboard, mouse, gamepad).
Custom Physics Engine – For collision detection, rigid bodies, and gravity (this will be your own implementation, no external library was mentioned).

# Development Plan:

I have outlined the development order for the game engine:
Create a Game Loop
Initialize OpenGL (Rendering)
Implement ECS (Entity Component System) using EnTT
Add Input Handling (Keyboard, Mouse, Gamepad)
Integrate a Physics Engine with collision detection and gravity.
Game Loop: i am working on creating a game loop as the first step.
