# What is Katip App?

This is a micro backup tool, which simply records any changes as they occur or with given intervals. It will be activated per folder
and users can later see the historical changes and compare them so that they never lose any changes they did when they are working in a particular directory they are tracking with Katip.

## How does the app work?

Currently, it is a CLI tool which exposes the following commands and arguments:

1. `katip watch [--path|-p folderpath] [--interval|-i milliseconds]` Starts a new watch. By default, it commits changes to the history
as any change occurs, and folderpath is the current directory.
2. `katip stop` Stops the watch.
3. `katip destroy` Destroys all the history recorded. It also stops the application if it is still running.
4. `katip pause` Pauses the app.
5. `katip resume` Resumes the app with all the arguments passed initially when the app was first started.

## Behind the Scenes

Internally, Katip uses [Git](https://git-scm.com) to record, store, retrieve, and reload historical changes in a given folder. It, however, automates all the Git specific commands and make it is easier to consume for regular users. It is an abstraction over Git to make it easier to use by everyone instead of just technical users. However, power users can also greatly benefit from Katip when they are in need a quick and fast version control solution to record, navigate, compare, and bring back their historical changes.

## Issues

The problem is that when the computer is restarted, the application will not continue watching the folder specified. At first, this will be documented, but later this will be improved by starting the application when the computer starts.

## Command line Interface
NAME:
   Katip - Micro backups with historical changes

USAGE:
   main.exe [global options] command [command options] [arguments...]

VERSION:
   0.0.1

COMMANDS:
   watch, w    Starts a new watch. By default, it commits changes to the history as any change occurs, and folder path is the current directory.
   stop, s     Stops the watch.
   destroy, d  Destroys all the history recorded. It also stops the application if it is still running.
   pause, p    Pauses the app.
   resume, d   Resumes the app with all the arguments passed initially when the app was first started.
   help, h     Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --help, -h     show help
   --version, -v  print the version