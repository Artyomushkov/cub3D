# cub3D
This group project is inspired by the world-famous eponymous 90's game, which was the first FPS ever. We explored ray-casting. The goal was to make a dynamic view inside a maze. I worked with mathematical engine of the game. 42's graphical library minilibx was provided for the project.

The constraints of project were:

• The management of your window must remain smooth: changing to another window, minimizing, etc.

• Display different wall textures (the choice is yours) that vary depending on which
side the wall is facing (North, South, East, West).

• Your program must be able to set the floor and ceiling colors to two different ones.

• The program displays the image in a window and respects the following rules:

◦ The left and right arrow keys of the keyboard must allow you to look left and
right in the maze.

◦ The W, A, S, and D keys must allow you to move the point of view through
the maze.

◦ Pressing ESC must close the window and quit the program cleanly.

◦ Clicking on the red cross on the window’s frame must close the window and
quit the program cleanly.

◦ The use of images of the minilibX is strongly recommended.

• Your program must take as a first argument a scene description file with the .cub
extension.

◦ The map must be composed of only 6 possible characters: 0 for an empty space,
1 for a wall, and N,S,E or W for the player’s start position and spawning
orientation.

This is a simple valid map:

111111

100101

101001

1100N1

111111

◦ The map must be closed/surrounded by walls, if not the program must return
an error.

◦ Except for the map content, each type of element can be separated by one or
more empty line(s).

◦ Except for the map content which always has to be the last, each type of
element can be set in any order in the file.

◦ Except for the map, each type of information from an element can be separated
by one or more space(s).

◦ The map must be parsed as it looks in the file. Spaces are a valid part of the
map and are up to you to handle. You must be able to parse any kind of map,
as long as it respects the rules of the map.

◦ Each element (except the map) firsts information is the type identifier (composed by one or two character(s)), followed by all specific informations for each object in a strict order such as :

∗ North texture:

NO ./path_to_the_north_texture

· identifier: NO

· path to the north texure

∗ The same for South, East, West

Floor color:
F 220,100,0

· identifier: F

· R,G,B colors in range [0,255]: 0, 255, 255

∗ Ceilling color:
C 225,30,0

· identifier: C

· R,G,B colors in range [0,255]: 0, 255, 255

◦ Example of the mandatory part with a minimalist .cub scene:

NO ./path_to_the_north_texture

SO ./path_to_the_south_texture

WE ./path_to_the_west_texture

EA ./path_to_the_east_texture

F 220,100,0

C 225,30,0

1111111111111111111111111

1000000000110000000000001

1011000001110000000000001

1001000000000000000000001

111111111011000001110000000000001

100000000011000001110111111111111

11110111111111011100000010001

11110111111111011101010010001

11000000110101011100000010001

10000000000000001100000010001

10000000000000001101010010001

11000001110101011111011110N0111

11110111 1110101 101111010001

11111111 1111111 111111111111


◦ If any misconfiguration of any kind is encountered in the file, the program
must exit properly and return "Error\n" followed by an explicit error message
of your choice.

Also some extra features were implemented:

• Wall collisions.

• A minimap system.

• Doors which can open and close.

• animated sprite.

• Rotate the point of view with the mouse.

## Usage

First, compile the project with make or make bonus - then the compilated program will include extra features.

Launch programm with ./cub3D or ./cub3D_bonus with the map argument. There are some maps configuration in maps folder.
