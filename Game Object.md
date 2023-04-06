### <u>Transform</u>

```cs
transform // specific transform of that obj
Transform // general transform class
```
transform (with small t) is attached to game object, but Transform (with capital T) is general transform class

### <u>Space</u>

This is what I missed when I first learnt Unity and it's the most important concept.

- Global space or Parent
	- Where object is relative to its parent
	- Transforming the parent also directly affects their children relative properties
- Local space or Object space
	- Position is based on where the object is and Rotation is based on which direction the object is looking