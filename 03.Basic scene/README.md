1. scene 
    - `const scene = new THREE.Scene()`
2. object
    - `const geometry = new THREE.BoxGeometry(1, 1, 1)`
    - `const material = new THREE.MeshBasicMaterial({ color : 'red' })`
    - `const mesh = new THREE.Mesh(geometry, material)`
    - `scene.add(mesh)`
3. camera
    - `const fov = 75`
    - `const size = { width: 800, height: 600 }`
    - `const camera = new THREE.PerspectiveCamera(fov, size.width / size.height)`
    - `scene.add(camera)`
4. renderer
    - `const canvas = document.querySelector('.webgl')`
    - `const renderer = new THREE.WebGLRenderer({ canvas: canvas })`
    - `renderer.setSize(size.width, size.height)`
    - `renderer.render(scene, camera)`
5. not thing shown?
    - camera inside object
    - `camera.position.z = 3`