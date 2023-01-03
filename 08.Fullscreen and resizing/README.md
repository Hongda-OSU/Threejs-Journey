### Fullscreen and Resizing
1. Viewport
    - `width: window.innerWidth`
    - `height: window.innerHeight`
    - css
2. Resize
    - `window.addEventListener('resize', () =>`
    - Update sizes
        - `sizes.width = window.innerWidth`
        - `sizes.height = window.innerHeight`
    - Update camera
        - `camera.aspect = sizes.width / sizes.height`
        - `camera.updateProjectionMatrix()`
    - Update renderer
        - `renderer.setSize(sizes.width, sizes.height)`
        - `renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))`
3. PixelRatio
    - `renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))`
4. Fullscreen
    - `window.addEventListener('dblclick', () => {`
    - `canvas.requestFullscreen()`
    - `document.exitFullscreen()`