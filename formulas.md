## Particle Attraction and Gravity
### Basic gravity
```
force = G × m1 × m2 / distance2
```

### JavaScript-friendly gravity implementation
```javascript
function gravitate (partA, partB) {
var dx = partB.x – partA.x,
dy = partB.y – partA.y,
distSQ = dx * dx + dy * dy,
dist = Math.sqrt(distSQ),
force = partA.mass * partB.mass / distSQ,
ax = force * dx / dist,
ay = force * dy / dist;
partA.vx += ax / partA.mass;
partA.vy += ay / partA.mass;
partB.vx -= ax / partB.mass;
partB.vy -= ay / partB.mass;
}
```
