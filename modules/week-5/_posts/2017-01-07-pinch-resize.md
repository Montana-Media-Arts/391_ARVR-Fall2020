---
title: Pinch and Resize
module: 5
jotted: true
---

# Resize

What if we want to resize our object?  Then, we must use multiple fingers to find and resize our AR object.

Using a method like this, we can achieve this goal.

```csharp
 public void _PinchtoZoom(GameObject ARObject)
    {
        if (Input.touchCount == 2)
        { // Store both touches. 
            Touch touchZero = Input.GetTouch(0); 
            Touch touchOne = Input.GetTouch(1);

            // Find the position in the previous frame of each touch.
            Vector2 touchZeroPrevPos = touchZero.position - touchZero.deltaPosition;
            Vector2 touchOnePrevPos = touchOne.position - touchOne.deltaPosition;
            // Find the magnitude of the vector (the distance) between the touches in each frame.
            float prevTouchDeltaMag = (touchZeroPrevPos - touchOnePrevPos).magnitude;
            float touchDeltaMag = (touchZero.position - touchOne.position).magnitude;
            // Find the difference in the distances between each frame.
            float deltaMagnitudeDiff = prevTouchDeltaMag - touchDeltaMag;
            float pinchAmount = deltaMagnitudeDiff * 0.02f * Time.deltaTime;
            ARObject.transform.localScale += new Vector3(pinchAmount, pinchAmount, pinchAmount);
        }
    }

```

How do we integrate this into our project?

