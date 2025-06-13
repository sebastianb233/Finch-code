# Finch-robot

### Development Checklist

| Completed | Task         | Description |
|:---------:| :-----------:|:------------|
|    ✅     | Familiarize  | Learn how to: <ul><li>Connect to the robot</li><li>Interpret what built-in sensors detect</li><li>Program basics in SNAP!</li><li>Setup local developing environment to code in Java</li></ul>|
|    ✅     | 3D Design    |  <ul><li>Get familiar with the thinkercat software</li><li>Thing what shape fit the best interest</li><li>Create our first model</li><li>Create The final model with some adjustments from the first model        |
|    ✅     | Develop Code |   <ul><li>Research how does the birdbrain library works</li><li>Create a skeach of what the robot would do</li><li>Research the platform where we are going to be coding</li><li>Create the first version of the code</li><li>Finalize with a V2 of the code what fixes all bugs or mistakes from version 1          |

---

<details>
<summary><strong>Inspiration for the Project</strong></summary>

I wanted to recreate the cornhole game what it could be played with little bals of paper.
Not only this is a game but if you have a created mind this robot could do different thinks such as 
a phone holder, and also a card holder it just depents on your imagination.
</details>

---

### Design Cycle
<img src="design_cycle (1).png" alt="design cycle" width="300" height="300">

###### Include commentary on your experience with the design cycle during this project

---
### Code to Highlight
```java
public boolean detectTape() {
        int tapeThreshold = 50; // Tape reflectivity threshold
        int leftLight = finch.getLight("L");
        int rightLight = finch.getLight("R");

        System.out.println("Left Light: " + leftLight + ", Right Light: " + rightLight);
        return leftLight >= tapeThreshold || rightLight >= tapeThreshold;
        
    }
}
```

---

### Motivation:
- In my experience my motivation was honostly using the 3D printer, becuase its my first time completing a project with them. This motivation give me more self confidence to create a better model that fit our interest and at the same time was ideal for the goal of the project.
### Why did we build this project:
- We build this project becuase it was the first thing that came to our minds , and it was something that anyother group did not thought about.
### What did we learn:
- In this project i learn that you are not always told what to do, or how to do things in a professional environment, This prohect teach to not depend on others and focus more on my self for my own benefit.
### What makes the project stand out:
- I things that it stands out because none of the other groups did something like ours and also i thing is the only one with intentionally multipurpose.
