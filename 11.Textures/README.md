### Textures
1. What are textures?
    - images that cover the surface the geometry
2. What do we need?
    - Color (or alebdo)
        - take the pixels of the texture and apply them to the geometry.
    - Alpha 
        - a grayscale image where white will be visible, and black won't.
    - Height
        - a grayscale image that will move the vertices to create some relief. 
        - You'll need to add subdivision if you want to see it.
    - Normal
        - add small details.
        -  It won't move the vertices, but it will lure the light into thinking that the face is oriented differently.
    - Ambient occlusion
        - a grayscale image that will fake shadow in the surface's crevices.
        - helps to create contrast.
    - Metalness
        - a grayscale image that will specify which part is metallic (white) and non-metallic (black).
        - This information will help to create reflection.
    - Roughness
        - a grayscale image that comes with metalness, and that will specify which part is rough (white) and which part is smooth (black). 
3. PBR
    - Physically Based Rendering
    - [PBR](https://marmoset.co/posts/basic-theory-of-physically-based-rendering/)
4. How to load texture?
    - `const texture = new THREE.Texture(image)`
    - `const material = new THREE.MeshBasicMaterial({ map: texture })`
5. Texture Loader
    - `const textureLoader = new THREE.TextureLoader()`
    - `const texture = textureLoader.load('/textures/door/color.jpg')`
    - could load multiple textures
6. Loading Manager
    - `const loadingManager = new THREE.LoadingManager()`
    - `const textureLoader = new THREE.TextureLoader(loadingManager)`
    - `loadingManager.onStart = () => {}`
    - `loadingManager.onLoad = () => {}`
    - `loadingManager.onProgress = () => {}`
    - `loadingManager.onError = () => {}`
7. UV Unwrapping
    - replace BoxGeometry by other geometries
    - `geometry.attributes.uv`
8. Transforming Textures
    - `colorTexture.repeat.x = 2`
    - `colorTexture.repeat.y = 3`
    - `colorTexture.wrapS = THREE.MirroredRepeatWrapping`
    - `colorTexture.wrapT = THREE.MirroredRepeatWrapping`
    - `colorTexture.offset.x = 0.5`
    - `colorTexture.offset.y = 0.5`
    - `colorTexture.rotation = Math.PI * 0.25`
    - `colorTexture.center.x = 0.5`
    - `colorTexture.center.y = 0.5`
9. Filtering and Mipmapping
    - minification filter
        - `colorTexture.minFilter = THREE.NearestFilter`
    - magnification filter
        - `colorTexture.magFilter = THREE.NearestFilter`
10. Texture formate
    - .jpg (lighter)
    - .png (heavier)