# Design (target wayland, optionally allow gamescope features if available)
---
## Browser layer
need to have a way to make web browsers not only useable with controller, but optimized as much as possible for it.
#### what this looks like:
we will call it a web view shell for lack of a better term and develop little ui around it
- for browser UI elements that are clickable, movable, etc. we need to allow the user to seamlessly interact with them they way 
they would expect to using a console or a console app (moving a focus box around ui elements). it doesnt need to be perfect but it should
simulate the experience of a tv app.
- in a window, have our custom ui componenents, drawn webpage, our navigation.
- ways to inject code into browser and make it easier for us
#### ways to do it (subject to change):
- CEF + Rust FFI
## UI layer
(i have no graphics programming experience)
looking into vulkan for our UI.
#### what this looks like:
- in place overlay
    - perhaps panel that slides out (think xbox)
    - displays system diagnositics (time/date, other stuff)

- landing (home page)
    - displays recently launched links, applications
    - place for system things (settings)
    - other fun things
#### ways to do it (subject to change):
- Winit + WGPU
- Slint
## Controller layer
give controller control of system, independent of window
#### what this looks like:
- controller daemon
- will have to build from the ground up
- 
#### ways to do it (subject to change):
- evdev (read) + uinput (write) + Unix sockets/DBus (IPC)

## QOL features
- controller pairing made easy



