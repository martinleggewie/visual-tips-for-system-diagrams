# Visual tips for system diagrams
Martin Leggewie, 2020-11-04

## Abstract

This article describes a collection of visual tips for creating so-called system diagrams.
As the goal of such diagrams is to convey information to the audience and be the basis for discussions, it is a good advice to keep the diagrams as simple as possible.
If you want/need to create such diagrams yourself, then these tips can support you in reaching this "as simple as possible" goal.


## Introduction

Before we start with the actual tips, let us first define what a system diagram is and what it is good for.


### Definition and goal: System diagram

A **system diagram** is a visual representation of a given real-world system landscape, typically located in the IT world.
In such a landscape a collection of systems and contained system components are connected to each other in order to achieve a specific functionality.
The goal of a system landscape is to make this functionality available to its users.

Now, the **goal of a system diagram** is to explain how the structure of a system landscape looks like, and how the users interact with it.
A system diagram is a visual communication tool, not more, not less.
Its sole purpose is to explain the system landscape, and be the basis for dicussions.

Typically, the **visual language of system diagrams** consists of

* stick figures,
* boxes,
* cylinders,
* clouds,
* arrows which connect shapes with each other, and
* texts which are place either inside or next to the shapes.

In addition, certain types of shapes (typically the boxes) can be placed inside other shapes which allows a recursive structure.


### Why should you care about how system diagrams look like?

Maybe you think that it is more important to create system diagrams correctly, compared to how they look like.
To follow this "A over B" catch phrase style used in the https://agilemanifesto.org and https://www.halfarsedagilemanifesto.org:

"Correct and useful content over simple and easy-to-understand visuals"

I absolutely agree.

Of course we first need to make sure that the our diagrams contain the correct information, specifically created for the intended type of audience.
But then, once we have the correct structure defined, we should also make sure that the audience does not need to suffer too much when trying to understand the information.

I would like to demonstrate what I mean with a concrete example.
Below you see an example of a system diagram:

![example system diagram - reduced to the max](diagrams/example-systemdiagram_reduced-to-the-max.png)

I don't know about you, but I think that this diagram is already quite readable, and the audience should be able to understand
* with which system the user interacts,
* which systems store something in the database,
* which system are somehow connected to which other systems,
* and what are the boundaries of the different elements.

Admittedly, this diagram is not very complicated because it contains only one user, three systems, one database, and in total six connection arrows.
With such a simple example, it should not be so important to put much emphasis on the visual style.

Well, let's see.

Let's have a look on another diagram which contains the exact same information.
But this time the creator applied a different visual style to the diagram elements.

![example system diagram - distracting and even hurting the eye](diagrams/example-systemdiagram_distracting.png)

In my point-of-view this diagram is much more difficult to read.
It is difficult to understand what all the elements are, and how they are related to each other.
The reason for this IMHO is a suboptimal usage of colors, fonts, shapes, and sizes and arrangement of elements in relation to each other.

Maybe you think that it was me who has created this second diagram in this difficult-to-read way on purpose, just to make a point, and that I exaggerated quite a bit.
The answer is: Yes, and no.

* Yes, I created the diagram intentionally like this, to make my point.
* No, I did not exaggerate.

If you don't believe me, please do an Internet search for the term "system diagram", and check the images your preferred search engine returns.
Some of them will be in a clean style, maybe similar to the first example diagram shown above.
But also there will be quite some images which are visually closer to the second example diagram.

Please don't misunderstand me:
I do not want to finger-point on others who have created such diagrams.
Most of us including me are not trained designers who had some education about the use of such visual elements.
Also, in my opinion, the visual tools out there not always provide a default configuration which would help us with creating simple designs.

But I do think that if we put effort in the creation process to come to simple diagrams which strip unneeded clutter, the audience will thank us because it will be easier for them to get the information.
After all, these diagrams are not meant to be pieces of art.
Instead their sole purpuse is to convey information and to trigger people to talk about the diagram's topic.

## What is in for you?

If you agree with me that the second diagram is somehow suboptimal, and if you also agree that the creator should and could have done better, then we are on the same page.

I strongly believe in the following rule:

> *It is better if one person (the creator) invests effort in the creation than if many persons (the audience) have to all invest the effort in understanding the creation.*

To follow this rule, I have experimented a lot with visual tools which can be used to create system diagrams over the past years.
From those experiment results I distilled some general tips and tricks I now (try to) apply when I need to create such diagrams.
These tips helped me creating diagrams with a clean and consistent structure.

Now, if you invest your precious time in reading this text, you will find the list of all these tips.
I am aware that these tips will most likely not change the world, but maybe you can take-away some ideas which support you the next time you have to create such diagrams yourselves.

Let's get started.


## General guidelines

The foundation of all the tips to come is a list of general rules.
These rules are the **mission statement** for the visual representation of a system landscape.


### Keep visual attributes as simple as possible

* No color gradients. TODO: Add example what happens if the same gradient is applied to boxes of different sizes.
* No 3d effects. TODO: Add example comparison of a system diagram with several boxes and arrows. Show that the 3d effect breaks down if you attach the connection arrow to the front.
* No drop shadows. TODO: Add example comparison.


### Add a legend to the diagram

Always add a legend to your diagram.
A legend explains the meaning of all visual elements and attributes used in the diagram.

---
_**Example:** The following system diagram I have already shown in the introduction section, but now it finally also contains a legend (which I should have added to the example in the first place anyway)._

![example system diagram - reduced to the max, now with legend](diagrams/example-systemdiagram_reduced-to-the-max_with-legend.png)

_You might notice another small change in the diagram compared to the first version shown in the introduction section:
The connection arrow from "User" to "System A" has a "uses" annotation.
I could have put this type of relation "User uses system" also as an additional entry in the legend, next to the "System calls system" annotation.
But as this "User uses system" relation type only exists once in the diagram, I find it easier for the reader if the type of relation (i.e., "uses") appears directly next to the connection arrow._

---

Without this legend, the audience has no other choice than to interprete the meaning of the elements of your visual language.
And if the audience needs to interprete, then this will surely cause misunderstandings.

Even if you use a well-defined visual language like UML for your diagrams, add a legend to your diagram.
Maybe you know all the elements of - for example - UML deployment diagram style (see https://en.wikipedia.org/wiki/Deployment_diagram), but you cannot assume that the audience knows this as well.
Adding a legend becomes even more important if you use your own visual language (like I do all the time).
If you don't define this language, the audience cannot know what a box with rounded corners means and how it is different from the boxes with sharp corners, or what is the difference between yellow and green fill style.

A very typical confusion arises when the diagram contains directed connections.
What does the direction stand for?
Do the arrow heads show the direction in which data flows, or do they show which systems call which other systems?
We cannot know until there is a legend which clearly defines this.


### Apply high-contrast coloring style

TODO: Describe that high contrast makes it easier for the audience to recognize the boundaries of the visual elements.
Best contrast is black and white, but typically you need color as an attribute to represent differences in one dimension.
Therefore you need more than just white. Use dark colors (dark: colors with a low luminosity value) for boundaries, use bright colors (bright: colors with a high luminosity value) as a background or fill color.

TODO: Add a comparison example, showing the same scenario in a high-contrast and a low-contrast situation.


---
CONTINUE HERE

---

## About text

### Choose font size inside boxes to be big enough compared to the size of the box

![text font size small vs big](diagrams/text_fontsize_small-vs-big.png)



## First, some hand-drawn images

This section shows all the concept art I have created to prepare writing this article.
Using a hand-drawn approach helped me because a) it actually makes fun to draw something, and b) forces me to use a different skill set than just typing on a computer keyboard. 

![slice 14](images/slice14.png)

![slice 01](images/slice1.png)
![slice 02](images/slice2.png)
![slice 03](images/slice3.png)
![slice 04](images/slice4.png)
![slice 05](images/slice5.png)
![slice 06](images/slice6.png)
![slice 07](images/slice7.png)
![slice 08](images/slice8.png)
![slice 09](images/slice9.png)
![slice 10](images/slice10.png)
![slice 11](images/slice11.png)
![slice 12](images/slice12.png)
![slice 13](images/slice13.png)
![slice 15](images/slice15.png)
![slice 16](images/slice16.png)
![slice 17](images/slice17.png)
![slice 18](images/slice18.png)
![slice 19](images/slice19.png)
![slice 20](images/slice20.png)
![slice 21](images/slice21.png)
![slice 22](images/slice22.png)
![slice 23](images/slice23.png)
![slice 24](images/slice24.png)
![slice 25](images/slice25.png)