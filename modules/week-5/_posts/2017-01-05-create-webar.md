---
title: Setup the Objects
module: 5
jotted: true
---

# Setup Objects

Now, we want to instantiate for all our objects as well as set everything to active.

```csharp

    arInstance = new GameObject[arPrefab.Count];
    for(int i = 0; i < arPrefab.Count; i++)
    {
        arInstance[i] = Instantiate(arPrefab[i]);
        arInstance[i].gameObject.SetActive(false);
    }

```


