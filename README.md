# RollaBall

## Aim: ##
To Roll a Ball using C# program in unity .

## Algorithm: ##
## Step1: ##

To Create a unity project in unity hub.

## Step 2: ##

Aftern creating Click File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (Expno2).

## Step 3: ##

Click Hierarchy -> 3DObject -> Sphere Hierarchy -> 3DObject -> plane Hierarchy.

## Step 4: ##

Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Sphere) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Cylinder to the plane and release the mouse

Create a folder in project and name as Materials Material folder -> Create -> Material (Name: Plane) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Drag the Capsule to the plane and release the mouse

## Step 5: ##

Create a folder name Coding and create a C# file to add the coding in it.

## Step 6: ##

To add our C# Script file to our selected object, click on the C# Script file and drag it to Sphere objects in the Hierarchy window and run the application.

## Step 7: ##

After run the application, you press the WASD and space key the ball will move and jump.

## Step 8: ##

Save the unity file and take screenshot.

## Step 9: ##
Close the Unity project.

# *PROGRAM*
```python
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float xForce = 5.0f;
    public float zForce = 5.0f;
    public float yForce = 200.0f;
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f;
        if(Input.GetKey(KeyCode.A))
        {
            x = x - xForce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + xForce;
        }
        float z = 0.0f;
        if (Input.GetKey(KeyCode.S))
        {
            z = z - zForce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z + zForce;
        }
        float y = 0.0f;
        if(Input.GetKeyDown(KeyCode.Space))
        {
            y = yForce;
        }

        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
```

## *Output:*
![image](https://github.com/veerapallijanith/RollaBall/blob/main/jani.png)

## *Result:*
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.
