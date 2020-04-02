DOM Maker
---------

#### Purpose
Provide a library that lets programmers build DOM dynamically using a syntax that is at least as short and readable as HTML, while providing all the benefits of using the JavaScript DOM construction methods, including inherent protection against HTML injection through text strings, and using functions with scope as event handlers.

The library should itself be short and easily readable. Rather than the library providing functionality for all eventualities, it should be easy to use the library with custom code for dealing with such eventualities, or to change the library to suit individual needs.

#### Example

    document.body.appendChild(
        FRAGMENT(
            P("A simple HTML structure with ",SPAN("nested")," elements.")
            ,P({className:"information"},"It is appended to the end of the body.")
            ,P({style:{backgroundColor:"yellow"}},"It contains inline styling.")
            ,BUTTON({onclick:function(){alert("Button clicked.")}},"Click me.")
        )
    )

For much more example code, and detailed instructions see [the guide and selftest file](http://nohatcoder.dk/dommaker/).

#### Content of repository
The entire library is contained in the file dom.js. Guide_selftest.htm contain a project description, and instructions on the use of the library. It also serves as a simple test of the library.

#### Versions

Version 0.6 contain a number of fixes for oddities of IE 8. It has been used in a number of projects, and no bugs have been found.

Version 0.8 removes IE 8 support. The `globalScope` function is removed, and the library now defaults to populate the global scope with upper case dom creation functions. The library may now be configured to generate error message DOM elements instead of throwing upon invalid input.

#### License
The library and the guide have a 2-clause BSD license.
