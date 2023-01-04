### Debug UI
1. Open Source
    - Dat.GUI
    - lil-gui
    - control-panel
    - ControlKit
    - Uil
    - Tweakpane
    - Guify
    - Oui
    - Bruno Simon's debug panel
2. lil-gui
    - `import GUI from 'lil-gui'`
    - `const gui = new GUI()`
    - we could add Range, Color, Text, Checkbox, Select, Button, Folder
    - `gui.add(mesh.position, 'y').min(-3).max(3).step(0.1).name('XXX')` (object, property, min, max, step, name)
    - `gui.addColor(paramaters, 'color').onChange(() => {material.color.set(paramaters.color)})`
    - we could also add function to gui (ex: spin)