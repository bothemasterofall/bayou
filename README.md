# Bayou

## About
Bayou is a game development framework using the allegro libraries for rendering,
keyboard and mouse capture, and playing audio. Its main purpose is to assist
with quickly developing a game utilizing 2D graphics.

## Dependencies
Install the following packages with your favorite package manager. Developer
platform utilized apt.
* g++
* liballegro5-dev
* liballegro5.0
* automake
* doxygen

## Installation
### Linux
If the above packages have been installed, then clone this repo, cd into it, 
and run `./build.sh`. Then run './bayou' from the src dir to run the sample
game.

### Mac
Never been attempted. Try installing it similar to linux.

### Windows
Bayou games may be developed on Windows, as my test games were until recently.
Utilised IDE is Visual Studio Community 2015 which is distributed by Microsoft
for free.

Bayou's source files need only be copied into a Visual Studio project to be
used, but Allegro may require extra steps to set up. Obey the following steps
to get Allegro set up in a Visual Studio project.

* Note: Developer does not have access to his Windows machine on June 18th,
though Allegro has very good documentation for how to get it set up in Visual
Studio. This list will be populated when developer is able to walk through
steps himself.

## What's contained
This repo contains the Bayou core files along with just enough to illustrate
how to use them in a simple game. The game you will build allows you to see how
the menus work in Bayou, and allows you to run around in an arena with a
central invisible wall and elf chasing you around.

## Documentation
Documentation may be generated by running `doxygen doxy_config` from the bayou
main directory. Each Bayou module has extensive doxygen documentation in the
source files.

## Usage/Development
A high level description will be given here, as more detail is included in
the documents generated in the aftermentioned documentation section.

Bayou games are developed by creating new subclasses of the State class. Each
state then uses the functions in the Manager module to change states when
certain logic happens.

## Weaknesses
Each of these weaknesses is planned to be corrected, and shall be done without
impacting the API.
* N^2 Collision detection within Environment class
* Client and Server communicate via TCP instead of UDP
* Client and Server classes only work on Linux
* No asset integration with the PhysFS
