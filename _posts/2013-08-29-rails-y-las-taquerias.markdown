---
layout: post
title: "Rails y Las Taquerías"
date: 2013-09-02 19:50
comments: true
categories: [tacos, rails, talks, pecha kucha, tech]
---
I take tacos relatively seriously. Seriously enough that I've organized multiple taco-themed parties in my lifetime.
Let's be real, though: any food whose remnants are licked from your fingers requires a
sense of humor.

As part of our immersion here in Quito we're doing [pecha kucha talks](www.pechakucha.org), which consist of 20 slides, presented for 20 seconds each,
resulting in a madcap 400-second talk on a topic of the presenter's choosing. I
chose to explain the Rails MVC framework with a taquería analogy.

This talk was originally given in Spanish, so I've provided a Spanish
transcript as well as a rough English translation below.

<!--more-->

<iframe src="http://www.slideshare.net/slideshow/embed_code/25738957"
width="427" height="356" frameborder="0" marginwidth="0"
marginheight="0" scrolling="no" class="slideshare" allowfullscreen
webkitallowfullscreen mozallowfullscreen> </iframe> 

<h2>En Español</h2>
Rails es una framework que tiene tres partes: el model, el view, y la
controller.
<ul>
<li> El model es el backend de la applicacíon. El model es el interface
  entre el database y tambíen trabajo con el data.</li>
<li> El view es el frontend de nuestra applicacíon. Es typicalemente en
  HTML o un otro lenguaje para "templating," y tambíen tiene un poco de
 Ruby (usualemente los variables). Es la presentacíon de la
applicacíon.</li>
<li> Finalmente, tenemos la controller. La controller es el pegamento entre
  el model y el view: el pasa el data desde el backend al frontend. Es
importante saber que Rails tiene una regla para los partes de la
applicacíon: model gordo, controller flaca.</li>
</ul>

Empezamos en la bodega. La bodega tiene todos los ingredientes para
nuestra taquería: los frijoles, el carne... Algun que trabajo en la
taquería necesita algo para prepara una comida. Toma lo que quiere y
deja la bodega. Pues, el puede preparar los ingredientes: el hace las
salsas y prepara la carne. Todo de este es el trabajo del **model**.
Recuerden, en Rails tenemos un model gordo. Es necesario hacer todo el
trabajo con los ingredientes en el model. 

Pues... una persona recibe la comida. La comida es preparado y listo
para servir. Esta persona no se importa como la comida fue preparar.
Esta persona solo quiere que la comida es disponsible y lista para sus
clientes. Tiene el trabajo para servir la persona que va a comer los
tacos. Este trabajo es como un **controller** en Rails. Recuerden que
Rails tiene una controller flaca: su trabajo es solamente dar el data al
view. 

Y que buena es el view-- mis tacos! Cuando estoy en un taquería, no me
importa sobre la preparacíon de los tacos. No me importa sobre la
receta. Si quiero cocinar los tacos, yo puedo cocinarlos en mi casa! No
es la objetiva para comer en un restaurante. Solo que me importa es la
comida, y si mi comida es buena. Es porque la experiencia del cliente es
como el **view**. El cliente no se se importa del trabajo para cocinar los
tacos, solamente si los tacos son buenos.

Si añadas la preparacíon, la servir, y el producto final, tienes algo
muy bueno... y un poco como el Rails MVC framework.

<h2>In English</h2>
The Ruby on Rails framework has three principal parts: the model, the
view, and the controller. The model takes care of most of the work,
interfacing with the database and modifying a lot of the data. The view,
on the other hand, is the presentation layer: it only has a bit of Ruby
(typically variables) but a lot of ERB to handle the way the app looks.
The controller is the glue between the two: passing data from the
database (from the model) to the page (the view).

Let's start at the pantry of the restaurant. All of the food is
contained there, and when a prep chef needs something, he or she goes
into the pantry, takes what they need, and returns to the kitchen to
prepare the food. The chef has the responsibility of chopping the meats,
mixing the salsas.. this is analogous to the **model** in Rails. Rails has
a convention for "fat model, skinny controller," wherein much of the
work should be done in the model before getting to the controller.

By the time the food reaches the server, it has been plated. The salsas
are lined up next to the tacos. The food is ready to go. All the server
cares about is getting the food to the customer in a timely manner,
without complaints. This is similar to the **controller** in Rails:
passing data from the backend out to the front, without doing much work
(remember, "fat model, skinny controller").

And, finally, the food makes its way to the customer. Much like the
server, the customer has very little curiosity regarding the recipe, the
preparation, or even how many more tomatoes are in stock: in fact, all
the customer typically cares about is how the tacos look and taste. This
is similar to Rails views, which hold very little Ruby and serve as the
presentation layer.
