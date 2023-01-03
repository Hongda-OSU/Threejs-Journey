### Geometries
1. What is Geometry?
    - Composed of *vertices* and *faces*
    - vertex (position, uv, normal, ...)
2. Built-in Geometries
    - BoxGeometry
    - PlaneGeometry
    - CircleGeometry
    - ConeGeometry
    - CylinderGeometry
    - RingGeometry
    - TorusGeometry
    - TorusKnotGeometry
    - DodecahedronGeometry
    - OctahedronGeometry
    - ...
3. BoxGeometry
    - 6 parameters (width, height, depth, widthSegments, hightSegments, depthSegments)
4. Subdivision
    - Have more triangles
5. BufferGeometry (Create Triangle)
    - use Float32Array
    - `const geometry = new THREE.BufferGeometry()`
    - `const positionsArray = new Float32Array([0, 0, 0, 0, 1, 0, 1, 0, 0])`
    - `const positionsAttribute = new THREE.BufferAttribute(positionsArray, 3)`
    - `geometry.setAttribute('position', positionsAttribute)`
6. Index
    - geometry have faces that share common vertices