 This component is normally used for checking the physics collisions.

To get the RigidBody component of an object:
```cs
RigidBody myRigidBody;

void Start() {
	myRigidBody = GetComponent<RigidBody> ();
}
```

<b><u>Note:</u></b> GetComponent is a generic method which allows us to pass in the RigidBody type. 

In the inspector tab, we can also freeze rotation on individual axis if you only want to object to be collided only, but not rotated according to the scene


To check if the object collides into another object, we can write the code to check in the OnTriggerEnter method

```cs
void OnTriggerEnter(Collider triggerCollider) {
	print(triggerCollider.gameObject.name);
}
```

If we don't want the object to be affected by physics, but still want to check for collisions, then we can disable Is Kinematic checkbox on the inspector tab

Also, we can add tags to the object to check what action should be executed based on the tag of the collided objects