# JFLAP Launcher for macOS

This repository packages JFLAP 7.1 as a macOS application. The app bundle
contains its own copy of `JFLAP7.1.jar` and launches it with an installed Java
runtime. The JFLAP JAR included here was taken from
https://www.jflap.org/jflaptmp/.

## Requirements

- macOS
- Java installed and available through macOS or Homebrew

You can confirm that Java is available by running:

```bash
java -version
```

## Install

1. Clone or download this repository.
2. Copy `JFLAP.app` into your `/Applications` folder. You can drag it there in
   Finder or run:

   ```bash
   ditto JFLAP.app /Applications/JFLAP.app
   ```

3. Open **JFLAP** from the Applications folder, Finder search, or Spotlight.

The application wrapper looks for Java in the standard macOS location and in
common Homebrew installation locations. If Java cannot be found, it displays
an error message instead of silently failing.

## Run Without the App Wrapper

To run the tracked JAR directly from the repository:

```bash
java -jar JFLAP7.1.jar
```
