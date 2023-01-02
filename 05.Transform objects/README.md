### Transform Objects
1. Move objects (x,y,z)
    - `mesh.position.x = 1` 
    - `mesh.position.set(0.7, -0.6, 1)`
2. `mesh.position.length()`
    - mesh to center
3. Distance to camera
    - `mesh.position.distanceTo(camera.position)`
4. Normalize (length 1)
    - `mesh.position.normalize()` 
5. Axes Helper
    - `const axesHelper = new THREE.AxesHelper()`
6. Scale objects
    - `mesh.scale.x = 2`
    - `mesh.scale.set(2, 0.5, 0.5)`
7. Rotation
    - `mesh.rotation.y = Math.PI` (half rotation 180)
    - rotation order matter!
    - `object.rotation.reorder('YXZ')`
8. Quaternion
    - update rotation <=> update quaternion 
9. LookAt
    - `camera.lookAt(mesh.position)`
10. Scene graphic (Group)
    - `const group = new THREE.Group()`
    - `scene.add(group)`
    - `group.add(cube1)`