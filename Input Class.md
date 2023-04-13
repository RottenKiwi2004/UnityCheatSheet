<u>Note</u> I will only include some common methods in here. Please look at the documentation for all methods in the class

```cs
Input.GetKeyDown(keyCode) --> bool
// keyCode: KeyCode
```

```cs
Input.GetAxis(axis) --> -1, 0, or 1
// axis: string ; "Horizontal" or "Vertical"
```

same also applies to 

```cs
Input.GetAxisRaw(axis) --> -1, 0, or 1
// axis: string ; "Horizontal" or "Vertical"
```

The only difference between GetAxis and GetAxisRaw is that GetAxis is smoothed out between -1, 0, and 1 based on the sensitivity, but GetAxisRaw will only return exactly -1, 0 or 1