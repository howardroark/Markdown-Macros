# Markdown should be readable

The beauty of Markdown is how well it ensures that text is left in a readable
state before parsing. There is much debate today about how to extend the
syntax in a plethora of different directions. The reality is that Markdown
itself is just fine the way it is. It lines up with way we have been structuring
literature for thousands of years.

There is no reason to extend the core syntax to cater for any scenario outside
of pure rational thought and argument. The core syntax should be readable and
understandable in raw form by any reasonable person.  As Albert Einstein
said... “If you can't explain it to a six year old, you don't understand it
yourself.”

#### Markdown promises a truly semantic web

Since the invention of HTML we have been struggling with the idea of how to
ensure that the structure lines up with the semantics of what we are trying
to convey. We conjure up ideas of hundreds of different elements that meet
all sorts of arbitrary needs. All the while markup is dumped into the web
without even properly making use of heading tags. Introducing more markup
does nothing but complicate the process.

Markdown is the opportunity to ensure that the web starts to fill with
markup that resembles the core of what people are trying to express. People
search the web in the way that they think, and it all revolves around
language and the written word.

#### Markdown is spreading

It appears inevitable that the use of Markdown and Git will increase in any
field that involves professional writing. It solves so many of the peripheral
problems that arise from the use of WSYIWIG editors and writing HTML directly.
The use of version control ensures that documents can easily evolve over time.

As we enter into specific fields we will start to find more and more scenarios
where specific features will be required within documents. Many of which will
need to be formatted in ways that go far beyond CSS and enter the realms of html
canvas, svg, webgl...

There should be a Macro standard that encourages people to extend Markdown in
readable formats. If the job of Markdown is to output purely semantic html, all
that really means is that it can be searchable by another human being... or
readable.

#### One output for all

Macros should be nothing more than a block of text that is acted on in the very
same manner as a paragraph of text. The Macro feature should encourage the use
of ideas like [GNU Bison](http://en.wikipedia.org/wiki/GNU_bison) when
designing each use case.

The DOM `textContent` of each Macro could be easily acted on after load to
produce the extended visual result. There is already a JavaScript variation
called [Jison](http://zaach.github.io/jison/) to aid in this endeavour.

#### An example

Here is an example which is inspired by the project [js-sequence-diagrams](http://github.com/bramp/js-sequence-diagrams) ...

**Input**

```
!!uml-sequence
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!

# Always readable
```

**Output**

```
<div data-macro="uml-sequence" class="macro-uml-sequence">
Alice->Bob: Hello Bob, how are you?
Note right of Bob: Bob thinks
Bob-->Alice: I am good thanks!
</div>

<h1>Always readable</h1>
```

**Some SVG work after the DOM load...**

![sequence](https://camo.githubusercontent.com/e8ee954236ea5f7fa37274c727c6267f2e3550e5/687474703a2f2f6272616d702e6769746875622e696f2f6a732d73657175656e63652d6469616772616d732f696d616765732f73616d706c652e737667)

# Always readable

#### Another practical example

Suppose you wanted a Macro that could normalize any video link into an embedded player?  Easy!

```
!!video
https://www.youtube.com/watch?v=JibxHpXqAfc
```

#### The browser can make awesome things

If your goal is to turn Markdown into PDF files or anything related to printing
you would be silly to not just build a solution that captures browser output
with something like [PhantomJS](http://phantomjs.org/). You can build very smart
solutions that use SVG and the block model. When it comes to visualizations all
of the best work is now centered around the browser.

#### There is no longer a need to compress HTML

If it is a matter of compression, there is no longer a real need. Mobile
networks are getting faster and the cloud keep on getting cheaper. Why compress
HTML?  Why loose any subtle amount of semantic data that could be hidden in the
whitespace?

#### No need for inline

There is no reasonable reason to extend Markdown to support the idea of inline
Macros. Outside of the agreed upon semantic features of writing itself nothing
else should need to exist inline with the text.
