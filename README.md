# League Manager
League Manager uses two seperate technologies and programming languages: one for the ui, and one for the logic. The UI is a web application built using the Vue.js framework,
while the logic is standard C++, using the Ultralight framework to display and facilitate communcation between the UI and the main application.

## Setting up Ultralight
Ultralight needs Visual Studio installed for the compiler, as well as [CMake](https://cmake.org/download/). When installing CMake, make sure you select the option to
add it to your PATH during install.

## Setting up Vue.js
The only prerequisite for Vue.js is the [Yarn](https://yarnpkg.com/) package manager, which you will want to download and install. You will also have to install npm if you don't have it already, though the Yarn installation should guide you through that.

## Setting up the program
1. Clone the GitHub repository. If you've never done this, using [GitHub Desktop](https://desktop.github.com/) is the easiest way to go about it.
2. Navigate to the "ui" folder using the command line.
3. Run `yarn install`. This will install all the required packages for the UI and may take a few minutes.
4. Navigate over to the "core" folder using the command line.
5. Run `mkdir build`, `cd build`, and then `cmake ..` to generate the Visual Studio project.

## Building the program
Building the program involves first building the ui, and then copying those files over to the main application and then building there.
1. Navigate to the "ui" folder on the command line.
2. Run `yarn build` which will generate a "dist" folder that contains several files and folders.
3. Copy the contents of the "dist" folder (but not the folder itself), and paste them in the "core/assets" folder, deleting any existing files before you do so.
4. Rename the index.html file to app.html (this should be fixed soon so you won't have to rename it, but its needed for now).
5. Navigate to the "build" folder you created during setup.
6. Run `cmake ..` and then `cmake --build . --config Release --clean-first` which will build the final project.
7. Open the "Release" folder inside the "build" folder and double click the LeagueManager.exe to test!
