### Camera
1. ArrayCamera
    - render the scene from multiple camera on specific area
2. SteroCamera
    - render the scene from two cameras that mimic the eyes to create a parallax effect (VR)
3. CubeCamera
    - do 6 renders (cubemap)
4. OrthographicCamera
    - render the scene without perspective
    - `new THREE.OrthographicCamera(left, right, top, bottom, near, far)`
    - remember to use aspect ratio if renderer is not square (assume l,r,t,b are all 1)
5. PerspectiveCamera
    - render the scene with perspectiven  
    - `new THREE.PerspectiveCamera(fov, aspect, near, far)`
    - *any object or part of the object closer than near or further than far will not show up*
    - do not use extreme value 0.0001 and 999999 to prevent z-fighting
6. Move camera position with mouse
    - `const cursor = {x: 0, y: 0}`
    - `window.addEventListener('mousemove', (event) => { cursor.x = event.clientX / sizes.width - 0.5 cursor.y = -(event.clientY / sizes.height - 0.5)})`
    - `camera.position.x = Math.sin(cursor.x * Math.PI * 2) * 3`
    - `camera.position.z = Math.cos(cursor.x * Math.PI * 2) * 3`
    - `camera.position.y = cursor.y * 5`
    - `camera.lookAt(mesh.position)`
7. Controls
    - FlyControls
        - enable moving camera like on a spaceship (rotate 3 axes, forward, backward)
    - FirstPersoncontrols
        - like FlyControls but with a fixed up axis (not FPS)
    - PointerLockControls
        - use the pointer lock JS API (no mouse)
    - OrbitControls
        - same like move camera with mouse position
    - TrackballControls
        - like OrbitControls without vertical angle limit
    - TransformControls
        - nothing to do with camera
    - DragControls
        - nothing to do with camera
8. OrbitControls
    - `import { OrbitControls } from 'three/examples/jsm/controls/OrbitControls.js'`
    - `const controls = new OrbitControls(camera, canvas)`
    - Damping
        - `controls.enableDamping = true`
        - in loop function, do `controls.update()`