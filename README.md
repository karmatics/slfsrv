slfsrv
============

### Create simple, cross-platform GUI applications, or wrap GUIs around command-line applications, using HTML/JS/CSS and your own browser.

__slfsrv__ is an executable that lets you create GUI applications (using simple HTML, CSS, and
Javascript) that launch the web browsers as the logic system and graphical front end. A Javascript API is
available to those application to provide enough access to the local computer system, files, and
executable, to create basic computer applications.

Jump To:

* [primary features](#primary-features)
* [usage, helpscreen version](#usage-helpscreen)
* [javascript api](#jsapi)
* [getting the files](#getting-files)
* [getting started with demos](#getting-started)
* [who to contact](#todo)
* [project homepage](#home)

------------------------------------------------------------------------------
<a name="primary-features"></a>
# Primary features:

* Run as server to deliver local HTML/CSS/JS in a local browser, as a localhost app.

* Provide JS API for access to the local computer system, including: data storage, file
and directory read/write, unpacking of bundled data (including other executables), and
ability to execute other programs.

* Run the same applications from within Windows, Mac/OSX, and Linux.

* Bundle applications into either single-file "slfsrv" files, or compile into
standalone executables. (Note, a Mac user can create a standalone Windows executable,
and vice versa).

* Blur the lines between what runs on the web, and what runs on the local machine. (i.e.
no longer must I launch a browser to run certain kinds of tasks, and some local start shell
to run local tasks, when now they can all launch from the browser).

<h1 style="color:red">...more documentation coming soon...</h1>

------------------------------------------------------------------------------
<a name="usage-helpscreen"></a>
# Usage, helpscreen version:

From `#slfsrv --help`

    slfsrv - Launch web browser and serve local HTML/CSS/JS/ASSET files to
             it; or compile everything into a standalone executable, for
             multiple platforms, as distributable localhost apps;
             or wrap a GUI around a command-line program.
             For more info, see https://github.com/BrentNoorda/slfsrv/

    USAGE: slfsrv [flags...] [filePath [initialUrlPath]
    WHERE: filePath - path to initial file or directory to serve; if file (e.g.
               index.html) then start with that file; if directory then
               look for index.html (or index.htm) in that directory; if not
               specified then look for index.html (or index.htm) in the
               current directory
               path may also be a *.slfsrv bundle created with -bundle
           initialUrlPath - when filePath is simply a directory, then initialUrlPath
               is the path to the first page to load within that directory
    flags:
      -help - this help text
      -bundle <out.slfsrv> - zip all contents of path into self-contained file
                             to be executed later with slfsrv - the .slfsrv
                             extension is required
      -compile <output-name> - compile slfsrv and all contents of directory
                               tree into a standalone executable
      -compile-from <ss-source> - used with the '-compile' flag, this specifies a
                                  slfsrv executable to use (else will use
                                  the current slfsrv executable); this flag is
                                  useful for making cross-platform distributals (e.g.
                                  creating a windows executable from OSX)
      -replace - used with the '-compile' or '-bundle' flags, this specifies
                 whether it is OK to replace the <output-name> file
      -port <port#> - specify port to run server on, else will look for a random port
                      that is not in use
      -verbose - write out lots of message about what's going on (else silent)
    EXAMPLES:
      slfsrv
      slfsrv /myapp
      slfsrv ../htmlgame/index.html
      slfsrv -compile /myapp
      slfsrv -compile /myapp -compile-from /tools/ss/win/slfsrv.exe
      slfsrv c:\user\me photo/tools/photoview.html
    VERSION: 0.0.1

------------------------------------------------------------------------------
<a name="jsapi"></a>
# JavaScript API:

[&#x25BA; Javascript API](docs/JSAPI.md) - calls made available to javascript running in the browser

------------------------------------------------------------------------------
<a name="getting-files"></a>
# Getting the files

### Building from source code

slfsrv source is available on [on github](https://github.com/BrentNoorda/slfsrv). It is written
in the "Go" language. So if you're familiar with Go it's just a standard build and you got it.

### Downloading pre-built executables

If you don't want to compile from original source, then download and unzip the "examples"
directory (you'll really want to run the examples), and then the executable appropriate to
your OS.

* [slfsrv-examples.zip](https://dl.dropboxusercontent.com/u/41075/slfsrv-downloads/slfsrv-examples.zip) - the examples you'll want
to start with for any of the following executables

* [slfsrv-darwin.zip](https://dl.dropboxusercontent.com/u/41075/slfsrv-downloads/slfsrv-darwin.zip) - for Macintosh/OSX users

* [slfsrv-windows.zip](https://dl.dropboxusercontent.com/u/41075/slfsrv-downloads/slfsrv-windows.zip) - (TBD) for Windows users

* [slfsrv-linux.zip](https://dl.dropboxusercontent.com/u/41075/slfsrv-downloads/slfsrv-linux.zip) - (TBD) for SUSE Linux

------------------------------------------------------------------------------
<a name="getting-started"></a>
# Getting started with demos

When you have the executable and examples, then from the examples directory run

    slfsrv -verbose EXAMPLES.html

This should launch a browser that will automatically step through some of the examples.

------------------------------------------------------------------------------
<a name="todo"></a>
# ISSUES / TODO / TOANSWER

[&#x25BA; TODO](docs/TODO.md) - what's still to be done

---------------------------------------------------------------------

random info to be better documented later:

For mac, to associate .slfsrv with an app so you can execute the bundle simply by double-clicking it
in the Finder, or by using the "open..." command in Terminal, follow these instructions for
[How to associate a file name extension with a darwin /linux/unix command-line executable on osx/macintosh](http://unlessimwrong.blogspot.com/2014/07/how-to-associate-file-name-extension.html)

------------------------------------------------------------------------------
<a name="contact"></a>
# Who to contact

[&#x25BA; Brent Noorda](http://www.brent-noorda.com/) - all about the author and how to contact

------------------------------------------------------------------------------
<a name="home"></a>
# Project Homepage

[&#x25BA; slfsrv project homepage](https://github.com/BrentNoorda/slfsrv) - slfsrv project on github

