TODO list
=========

Immediate
---------

* Add a preference for setting the `PATH` variable.
  Perhaps even read it from `~/.profile` if possible?

* Upload a binary package

* Level β:

    * Implement `runStmt` function to bind values while doing IO actions.
      Cannot be implemented by evaluating expressions.

    * Implement a way to evaluate cells concurrently.
      We still want to be able to bind variables sequentially.
      Using `forkIO` explicitely would do, but then we can't stop it again.

Later
-----

* For IO actions:
  Set working directory to be the directory where the worksheet file was located

* Integrate a viewer for Haddock documentation

* Integrate a way to query type signatures

* Implement a `loadFile` operation
  * Maybe even implement editor for files?

* Switch programming of user interface to some other language / approach.
  * sodium.js ?
  * threepenny-gui ?

* FIXME: Maybe do *not* move the cursor after evaluating a cell?


Much later
----------

* Bundle the `hyper-haskell-server` executable and a package database with the front-end,
  so that the user has a default Haskell interpreter to work with.
  The user is still free to choose another database if he likes to.
  
  Implementing this would require [relocatable Haskell packages][relocatable].
  Unfortunately, they are not readily supported yet,
  and I don't want to spend much time with it.
      
  [relocatable]: https://github.com/haskell/cabal/issues/462

