
### To Run

* execute: `build_run.sh`

### Notes

* This creates a modular jar, `lib/net.codetojoy.example.jar`
* The jar contains `net.codetojoy/example/resources/640px-Baden.Beethoven01.jpg`
* The module does *not* open `net.codetojoy/example/resources`
* `App.java` uses the module and attempts to load the image. It *fails* because the package is not opened. i.e. strong encapsulation is protecting the resource

### Layout

* the main app resides in the default package:
```
src/main/App.java
```

* typical module structure:
```
src/net.codetojoy.example/module-info.java
src/net.codetojoy.example/net/codetojoy/example/Composer.java
```

* the build script copies the image into place during jar creation
```
src/net.codetojoy.example/net/codetojoy/example/resources/640px-Baden.Beethoven01.jpg
```

* we use a place-holder class to placate the compiler
```
src/net.codetojoy.example/net/codetojoy/example/resources/PlaceHolder.java
```
