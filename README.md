# Purpose of fps-lib-se
The purpose of this library is to create a set of stand alone re-usable functions, interfaces, types and constants that can be used in SPFx web parts and the FPS-Banner component.
The intent is to be able to more easily use a standard code base with less dependancies that could be used across many versions of SPFx including both SPO and SE.

## The key differentiator:
There are no hard dependancies (requiring importing) of any specific version of Pnp, React, Graph, SPFx Context or MSFT libraries.
There are dependancies for typescript though just to be able to leverage typing.
This does not mean that I have not copied specific interfaces from those sources for general use... particularly interfaces.
Some examples are PnpJS Interfaces for things like Fields (IFieldInfo) which are generally unchanged since SP On Prem.
Another example are portions of the web part and page context used for interfaces.
There may be things from later versions (like column formatting) that may be added as an optional property so it can be reused.

## Code base
This library is primarily derived from extracts of fps-library-v2 and fps-pnp2 libraries.

## /types/ folder --- old /common/ folder
I did create a new top folder /types/ which is intended for commonly used interfaces that are not specific to one function.
I did try to move most types in there but found it would disrupt to many imports (such as IAnyShourceItem).
So at this point, my goal is to put common interfaces there (like ISourceProps, ISourceState) and use that as much as possible in the future.
However, interfaces intended for specific functions in this library may be in the folder with the function.
For interfaces that are derived from a specific version of a source like Pnp, I typically put those in a folder indicating the version number it is derived from.

## /banner/ folder
Interfaces specific to the /banner/ folder will likely be nearest to the code because it is typically saved in the same location as in fps-library-v2 for easier import updates.


## /logic/ and /components/ folders
These are files derived from fps-library-v2/src/samefolder which could be extracted here for easy reuse across versions.
I am trying to mirror the logic and components folder structure of fps-library-v2.
The goal will be to eventually create fps-library-v3/fps-PnpX for future major changes to React or Pnp and have them import any re-usable code from this library.

## See CHANGELOG.md for a complete history of this librrary
