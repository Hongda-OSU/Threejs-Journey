### Material
1. MeshBasicMaterial
    - `const material = new THREE.MeshBasicMaterial()`
    - `material.color = new THREE.Color('#ff0000')`
    - `material.wireframe = true`
    - `material.transparent = true`
    - `material.opacity = 0.5`
2. MeshNormalMaterial
    - `const material = new THREE.MeshNormalMaterial()`
    - `material.flatShading = true`
3. MeshMatcapMaterial
    - `const material = new THREE.MeshMatcapMaterial()`
    - `material.matcap = matcapTexture`
4. MeshDepthMaterial
    - `const material = new THREE.MeshDepthMaterial()`
5. MeshLambertMaterial
    - need add light
    - `const ambientLight = new THREE.AmbientLight(0xffffff, 0.5)` (add to scene)
    - `const pointLight = new THREE.PointLight(0xffffff, 0.5)` (need position)
    - `const material = new THREE.MeshLambertMaterial()`
6. MeshPhongMaterial
    - `const material = new THREE.MeshPhongMaterial()`
    - `material.shininess = 100`
    - `material.specular = new THREE.Color(0x1188ff)`
7. MeshToonMaterial
    - `const material = new THREE.MeshToonMaterial()`
    - `material.gradientMap = gradientTexture`
    - `gradientTexture.minFilter = THREE.NearestFilter`
    - `gradientTexture.magFilter = THREE.NearestFilter`
    - `gradientTexture.generateMipmaps = false`
8. MeshStandardMaterial
    - use PBR
    - `const material = new THREE.MeshStandardMaterial()`
    - `material.metalness = 0.45`
    - `material.roughness = 0.65`
    - aoMap
        - `material.aoMap = doorAmbientOcclusionTexture`
        - `sphere.geometry.setAttribute('uv2', new THREE.BufferAttribute(sphere.geometry.attributes.uv.array, 2))`
        - `material.aoMapIntensity = 1`
    - `material.displacementMap = doorHeightTexture` (need more vertices [subdivision])
    - `material.displacementScale = 0.05`
    - `material.metalnessMap = doorMetalnessTexture`
    - `material.roughnessMap = doorRoughnessTexture`
    - `material.normalMap = doorNormalTexture`
    - `material.normalScale.set(0.5, 0.5)`
    - `material.transparent = true`
    - `material.alphaMap = doorAlphaTexture`
9. MeshPhysicalMaterial
    - clear coat effect
10. PointsMaterial
    - create particle
11. ShaderMaterial & RawShaderMaterial
    - create shader
12. Environment Map
    - `const cubeTextureLoader = new THREE.CubeTextureLoader()` (use CubeTextureLoader to load)
    - `material.envMap = environmentMapTexture`