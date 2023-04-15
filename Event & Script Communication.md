Example: If we have 2 scripts, first is `Player` script and another is `GameUI` script

Here's the example code for `Player`
```cs
public class Player : MonoBehaviour {
	public float health = 10;
}
```

and here's the `GameUI` class
```cs
 public class GameUI : MonoBehaviour {
	// This will be the variable of that class to store the reference of that object later
	Player player;
}
```

Now we will need to find the reference for our objects

If we know the name of that object
```cs
// Find GameObject by name
GameObject playerObject = GameObject.Find("Player");

// Only get the Player component from the GameObject
player = playerObject.GetComponent<Player>();
```

If we know the tag of that object, we can find object by tag
```cs
GameObject playerObject = GameObject.FindGameObjectWithTag("Player");
player = playerObject.GetComponent<Player>();
```

And finally, the most straightforward way is to find object of type
```cs
player = FindObjectOfType<Player>();
```

### Event

To create an event that will be referenced to later, we need to first import System
```cs
using System;
```

Then create an event Action

```cs
public event Action OnPlayerDeath;
```

To invoke the event
```cs
if (health <= 0) {
	OnPlayerDeath();
}
```

Now inside GameUI class, we can subscribe `GameOver` method to the `OnPlayerDeath` event
```cs
void Start () {
	player.OnPlayerDeath += GameOver;
}

void GameOver() {
	// Implementation
}
```

<b><u>Important</u></b> If nothing is subscribed to the event and we try to invoke it, the event will be null and causes an error.

To prevent this, we simply add an if-statement
```cs
if (OnPlayerDeath != null) {
	OnPlayerDeath();
}
```