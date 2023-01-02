### Animation
1. `requestAnimationFrame`
    - call a function on the next frame
    - `window.requestAnimationFrame(loop)` (based on frame rate)
2. Frame rate
    - `const clock = new THREE.Clock()`
    - `const elapsedTime = clock.getElapsedTime()`
    - `mesh.rotation.y = elapsedTime`
3. Circle
    - `mesh.position.y = Math.sin(elapsedTime)`
    - `mesh.position.x = Math.cos(elapsedTime)`
4. GSAP
    - `$ npm install --save gsap@3.5.1`
    - `gsap.to(mesh.position, {duration: 1, delay: 1, x: 2})`