---
title: Mulitple Prefabs
module: 5
jotted: true
---

# Multiple Prefabs

In this section, we want look at how to add multiple prefabs. In order to do that, we must create a list of prefabs

```csharp

 private List<GameObject> arPrefab;

```

Then, we want to create an array of GameObjects instances

```csharp

private GameObject[] arInstance;

```

# Check for touch and Iterate

Finally, let's add a boolean to check to see if the screen has been touched and iterate through our array.  Don't worry; we will revisit this later!

```csharp

private bool isTouched = false;
private int index = 0;

```