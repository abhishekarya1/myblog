---
title: Building webpages with AI
subtitle: A look into Sketch2Code, an open source project by Microsoft's AI Lab
date: 2018-09-14
bigimg: [{src: "/img/postimg/s2c.png", desc: "Machine Learning"}]
tags: ["Machine Learning", "Deep Learning"]
---

## What seems to be the problem with building HTML pages?
I think it has to do with the amount of work one has to do for building just the structural components. With machine learning, we can easily identify these components like lines, text, and boxes, and create code for it. But web designers can do that more efficiently.

The problem is brainstorming designs. When having a lot of ideas in the mind, you can draw them on a paper or whiteboard in a jiffy, but the same is not true for code, which is a hefty amount of effort and not something designers want to do as it delays the design process.

I used Microsoft Frontpage for creating webpages in my school days and it was quite a relief for a newbie like me. I think the Sketch2Code is a step up from that, in the right direction.

## Sketch2Code
Microsoft AI's Sketch2Code is a solution that uses AI to transform a handwritten user interface design from a picture to valid HTML markup code. It is open source and you can play around with the tool as well as the code behind the tool as much as you like. You can find the code, process flow, architecture, and all the details on [GitHub](https://github.com/Microsoft/ailab/tree/master/Sketch2Code).

![Process GIF](/img/s2c/s2c.gif)

The web application is free and available to everyone, you can try out Sketch2Code right away on this [website](https://sketch2code.azurewebsites.net/).

Home Page - [AI.lab](https://www.ailab.microsoft.com/experiments/30c61484-d081-4072-99d6-e132d362b99d)

Official Blog Post - [Azure](https://azure.microsoft.com/en-us/blog/turn-your-whiteboard-sketches-to-working-code-in-seconds-with-sketch2code/)

Watch this short video to know more about the project - [Microsoft Developers](https://www.youtube.com/watch?v=V6pqqPPHyYM).  

### Workflow
#### 1. Detect Design Patterns
A Custom Vision Model trained to perform object recognition against HTML hand-drawn patterns is used to detect meaningful design elements into an image.

#### 2. Understand handwritten text
Each detected element is passed through a Text Recognition Service to extract handwritten content.

#### 3. Understand Structure
The information of the detected objects and their position inside the image is feed into an algorithm that generates the underlying structure.

#### 4. Build HTML
A valid HTML is generated accordingly to the detected layout containing the detected design elements.

![Workflow](/img/s2c/s2c_workflow.jpg)
**Image: Sketch2Code Workflow**

It utilizes cloud computing with the Azure Platform via the Azure Cloud Platform and Azure Cloud AI Services.

![Architecture Diagram](/img/s2c/s2c_cloud.jpg)
**Image: Sketch2Code Architecture Diagram**

The model identifies the basic HTML elements such as buttons, labels and text boxes, allowing it to predict when those elements are present in any given image. It also can recognize handwritten text within the boxes to create a fully formed app or a webpage

The best part about the application is that the code is extractable not just in HTML but also in XAML and UWP (Universal Windows Platform). So you can get the codes from scratch and use it anyway to create your own applications.

## Let's test it

My test involves five images, all hand drawn on paper.

#### Image-1
A page having an image, some text and two buttons.

![Image1](/img/s2c/s2cimg1.png)

See the generated [HTML page](/img/s2c/s2c_html/s2cimg1.html).

<br>

#### Image-2
A page having a lot of radio buttons.

![Image2](/img/s2c/s2cimg2.png)

See the generated [HTML page](/img/s2c/s2c_html/s2cimg2.html).

<br>

#### Image-3
A page having an image, text and some radio buttons. The tool performed pretty well on this one.

![Image3](/img/s2c/s2cimg3.png)

See the generated [HTML page](/img/s2c/s2c_html/s2cimg3.html).

<br>

#### Image-4
A page having a table.

![Image4](/img/s2c/s2cimg4.png)

See the generated [HTML page](/img/s2c/s2c_html/s2cimg4.html).

<br>

#### Image-5
A very arranged and nicely laid out page. The tool performed well on this one too.

![Image5](/img/s2c/s2cimg5.png)

See the generated [HTML page](/img/s2c/s2c_html/s2cimg5.html).

## Conclusion
The open source initiative by Microsoft's AI.lab is a step in the right direction. And there is more to come our way, as more and more AI-based tools aid the web development processes. Sketch2Code shows promise as it works on almost any image and recognizes text even with not-so-good handwriting with enough accuracy.

One thing I liked the most about Sketch2Code is that it is fast, faster than I expected it to be. And in this case, you have nothing to do but applaud the people behind it and a potentially huge open source community that it invites today to work on it and to improve it further.
