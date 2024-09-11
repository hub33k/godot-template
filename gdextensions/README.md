# gdextensions

- https://docs.godotengine.org/en/stable/tutorials/scripting/gdextension/gdextension_cpp_example.html

## Requirements

- scons
- C++ compiler

## Getting Started

```sh
# cwd to gdextensions folder
cd gdextensions

# Generate extension api `gdextensions/extension_api.json`
/Applications/Godot_mono-4.3.app/Contents/MacOS/Godot --dump-extension-api --headless

# Building the C++ bindings
cd godot-cpp
# platform: windows, linux or macos
# You may need to add bits=64 to the command on Windows or Linux.
scons platform=macos custom_api_file=../extension_api.json
cd ..

# Build gdextension
cd modules/example
scons platform=macos
```
