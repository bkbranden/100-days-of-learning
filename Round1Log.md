# 100 Days Of Code - Log

### Day 7: July 8th, 2020

**Today's Progress**: Got a refresher on some Javascript basics and syntax fundamentals. While going over precedence rules, the idea of precedence rules really caught my attention and I went into a rabbit hole of trying to figure out how the compiler automatically generates precedence rules. In a very generalized solution, additional non-terminals are added so that higher levels of recursion are added to the parse tree so things that are higher precedence are lower depth. This lower depth makes the code generation evaluate that expression first as the code generation recurses depth-first through the parse tree which allows it to reach that higher precedence operator first.

**Thoughts:** The basics of Javascript was honestly kind of dry since I knew about all of the information covered since it was basic stuff like conditionals and operators and variables. The aside in to the precedence rules was very interesting since there seemed to be an optimal way to solve the problem based on the type of parser being used. An SLR(1) parser seemed to get the job done differently by utilizing a precedence look-up table.

**Link to work:** [Today's Notes](files/Round1Learning/Level4/JavascriptBasics.md)

### Day 6: June 25, 2020

**Today's Progress**: Today, I put the application of the CSS that was covered before into styling a form. In addition, I learned about a CSS framework called Tailwind CSS that allows for CSS styling based on what class names are given to the HTML elements. The same form was styled utilizing Tailwind.

**Thoughts:** It was interesting to combine the small nuances and foundations that I learned in CSS get applied to styling a basic form and also doing so with a new framework. While this isn't the most exciting stuff, I am trying to bolster the foundations and then see how well it gets applied.

**Link to work:** [Today's Notes](files/Round1Learning/Level3/MoreCSS.md)


### Day 5: June 24, 2020

**Today's Progress**: Covered more breadth of CSS information and I was able to learn about something that I didn't know existed in CSS before "filters". I didn't know that there was a convenient way to add "photoshop-like" filters to elements in the DOM tree. Also, I learned about creating custom-variables in CSS as well as how CSS properly error handles.

**Thoughts:** Today I wasn't able to cover as much breadth of information as I wanted mainly because I wanted to digest the CSS information as well as I could, but for me it took some pushing through to get motivated to cover it earnestly.

**Link to work:** [Today's Notes](files/Round1Learning/Level3/MoreCSS.md)

### Day 4: June 23, 2020

**Today's Progress**: Dove deeper into more of CSS and beefing up my foundations with CSS. Today, I reviewed over things like the display and tables. I finally understand what the use of "floats" were in respect CSS Grid and Flexbox. Also, learned exactly what the different values in positioning do and messed around with some of them.

**Thoughts:** Some of the information that I review is actually very helpful and covers things that I did not know previously. Things like how floats work and what they are used for were some examples of things I didn't really understand about CSS, but have been cleared up.

**Link to work:** [Today's Notes](files/Round1Learning/Level3/MoreCSS.md)

### Day 3: June 22, 2020

**Today's Progress**: Finished reviewing the basics of CSS including how to add resources such as images, pseudo elements, Units, calc(), etc. and started diving into the box model of CSS

**Thoughts:** Again this reviewing is very refreshing since the majority of my understanding of CSS was based on just trying things and trying to make it work in context of the project that I was working on. Reviewing this, there are somethings that I learned such as using the viewport height and width as well as the units for lengths. Furthermore, reviewing the foundational concepts such as how the box model works will be very beneficial when I get to reviewing CSS grids and the flex-box model.

**Link to work:** 1: [Today's Notes](files/Round1Learning/Level3/IntroToCSS.md) 2: [Today's Notes](files/Round1Learning/Level3/MoreCSS.md)

### Day 2: June 21, 2020

**Today's Progress**: Started cracking CSS rules and selectors

**Thoughts:** Reviewing the CSS from the basics is a good foundational cover for me. Again like HTML, there are a lot of information that I had already knew, but I learned some bits of information that I was previously unaware of such as how the Cascading works on CSS styling, Attribute Selectors, and how pseudo-class selectors work.

**Link to work:** [Today's Notes](files/Round1Learning/Level3/IntroToCSS.md)

### Day 1: June 20, 2020

**Today's Progress**: Learned and took notes on the basics of the web, networks, and HTML

**Thoughts:** Was pretty boring since I knew most of the material, but I learned some more interesting details on anchor tags such as having mailto: protocols and how to point to something within the page by prepending "#". Also I was able to soldify my understanding of very basic HTML forms.

**Link to work:** [Today's Notes](files/Round1Learning/Level2/NetworkingBasics.md)