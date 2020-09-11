---
title: Check Touch
module: 5
jotted: true
---

# Check Touch

In the Update method, we need to check if the screen has been touched. If so, then we want to set our boolean value to true.

```csharp

    if (Input.touchCount > 0)
    {
        isTouched = true;
        
    }

```

Then, we need to add an object to a screen and increment the index.

```csharp

    if(isTouched)
    { 
        arInstance[index].gameObject.SetActive(true);
        arInstance[index].transform.position = pose.position;
        arInstance[index].transform.up = pose.up;
        isTouched = false;
        index++;
    }
    
```

Don't forget to change the else statement of the RayCast so that it reflects the object.

```csharp

 arInstance[index].gameObject.SetActive(false);

 ```
