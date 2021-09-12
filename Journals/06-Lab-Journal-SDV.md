# SDV601 - Week 6 Blog

------

## **Graphs and Charts**

------

What have I learned?

This week I learned about the implementation of graphs and charts using the `matplotlib` library.

### Matplotlib

Matplotlib is a very useful tool for data analysis and is very easy to use. Many of the examples are very straight forward and allow us to visually represent data. There are many different simple and complex ways we can display this data from simple line graphs to 3D interactable models of data.

Below is several examples with their implementation:

<u>Simple Line Graph:</u>

```python
import numpy as np
import matplotlib.pyplot as plt

plt.plot([1, 2, 3, 4])
plt.show()
```

![line](https://i.imgur.com/UyobpiC.png)

<u>Dark Theme (My preferred):</u>

```python
import matplotlib.pyplot as plt
import numpy as np
plt.style.use('dark_background')

plt.plot([1, 2, 3, 4], [1, 4, 9, 16])
plt.show()
```

![dark](https://i.imgur.com/nieR08u.png)

<u>Sub Plots:</u>

```python
import numpy as np
import matplotlib.pyplot as plt

names = ['x', 'y', 'z']
values = [1, 10, 100]

plt.figure(figsize=(9, 3))

plt.subplot(131)
plt.bar(names, values)
plt.subplot(132)
plt.scatter(names, values)
plt.subplot(133)
plt.plot(names, values)
plt.suptitle('Sub Plots')
plt.show()
```

![sub](https://i.imgur.com/dmqj5Rn.png)

<u>Bar Graph:</u>

```python
import matplotlib.pyplot as plt
import numpy as np


labels = ['G1', 'G2', 'G3', 'G4', 'G5']
men_means = [20, 34, 30, 35, 27]
women_means = [25, 32, 34, 20, 25]

fig, ax = plt.subplots()
rects1 = ax.bar((np.arange(len(labels)) ) - 0.35/2, men_means, 0.35 , label='Men')
rects2 = ax.bar((np.arange(len(labels)) ) + 0.35/2, women_means, 0.35 , label='Women')

ax.set_ylabel('Scores')
ax.set_title('Scores by group and gender')
ax.set_xticks(np.arange(len(labels)) )
ax.set_xticklabels(labels)
ax.legend()

ax.bar_label(rects1, padding=3)
ax.bar_label(rects2, padding=3)

fig.tight_layout()

plt.show()
```

![bar](https://i.imgur.com/ehxyDk2.png)

<u>3D Modelling</u>:

```python
import numpy as np
import matplotlib.pyplot as plt

ax = plt.figure().add_subplot(projection='3d')

theta = np.linspace(-4 * np.pi, 4 * np.pi, 100)
z = np.linspace(-2, 2, 100)
r = z**2 + 1
x = r * np.sin(theta)
y = r * np.cos(theta)

ax.plot(x, y, z, label='3D Model')
ax.legend()

plt.show()
```

![3d](https://i.imgur.com/qs0ZEvO.png)


------

How have I learned this?

I have learned this by looking at tutorials online and following the steps to implement the different graph types. I have practiced using the different types and how to implement them.


------

Why have I learned this?

Python is a well used language when it comes to data analysis. The ability to implement a library such as matplotlib (or others such as plotly, seaborn, or ggplot) allows us to visually understand the data rather than reading numbers. 


------

What will I do to remember this learning?
I will continue to practice these techniques and find areas where I can implement this knowledge.

------

What do I know now, that I did not know before?

- I learned how to model a 3d graph
- How to change the them of the graphs from light to dark them
