# Markdown should be readable

I have been thinking about the idea of a Macros for a long time.  I feel it is inevitable that the use of Markdown and Git will increase in any field that involves professional writing.  It solves so many of the peripheral problems that arise from the use of WSYIWIG editors and writing HTML directly.  Git just makes sense because documents need to evolve over time. It's a perfect reason to ensure that your lines are less than 80 characters (or maybe an even better number).  I see no reason to extend the core syntax to cater for any scenario outside of pure rational thought and argument. The core syntax should be readable and understandable in raw form by any reasonable person.  As Albert Einstein said... “If you can't explain it to a six year old, you don't understand it yourself.”

There is going to be an increasing list of items that fall outside of this category. Many of which will need to be formatted in ways that go far beyond CSS and enter the realms of html canvas, svg, webgl... There should be a Macro standard that encourages people to extend Markdown in readable formats. If the job of Markdown is to output purely semantic html, all that really means is that it can be searchable by another human being... or readable. 

If we follow the UNIX philosophy well we may want to argue that Macros should just be their own process that happens before or after the parsing of Markdown itself.  I think that if the objective of both is to output HTML then it should happen at the same time to avoid security problems.  

The DOM `textContent` of each Macro could be easily acted on after load to produce the extended visual result.  Encourage the use of the ideas like [GNU Bison](http://en.wikipedia.org/wiki/GNU_bison) when designing the syntax of each Macro extension.  There is already a JavaScript variation called [Jison](http://zaach.github.io/jison/).

This process would act as a way to protect the Markdown standard from becoming riddled with complex extensions.  There is a lot of risk that Markdown starts being used as a tool for web development or expressly for programmers.  If this starts to happen it could start to invalidate the potential for purely semantic HTML that Markdown has looked so promising to offer.  A lot of consideration needs to be made towards the reality that we are trying to make information more searchable here.

#### An example

I would like to offer the idea as an example which is inspired by the project [js-sequence-diagrams](http://github.com/bramp/js-sequence-diagrams) ...

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

**Some SVG work after the DOM load**

![sequence](https://camo.githubusercontent.com/e8ee954236ea5f7fa37274c727c6267f2e3550e5/687474703a2f2f6272616d702e6769746875622e696f2f6a732d73657175656e63652d6469616772616d732f696d616765732f73616d706c652e737667)

# Always readable

*And writable*... Markdown should focus on maintaining a natural flow of thought. The less often you have to wonder about how to do something, the less often you loose your concentration.  The beauty of Markdown is that it just lets you keep typing, the syntax is so simple.  Any extension should do its utmost to ensure a syntax that just makes sense to the user.  

#### Another practical example

Suppose you wanted a Macro that could normalize any video link into an embedded player?  Easy!

```
!!video
https://www.youtube.com/watch?v=JibxHpXqAfc
```

#### The DOM can make awesome things

If your goal is to turn Markdown into PDF files or anything related to printing you would be silly to not just build a solution that captures browser output with something like [PhantomJS](http://phantomjs.org/). You can build very smart solutions that use SVG and the block model.  I had a little success in a [quick attempt](https://github.com/codingcoop/get-diagrams) to port this idea to Markdown through HTTP GET parameters and image tags. It still has a bunch of bugs though and zero optimization.  The point is that I'd rather just do some DOM work after the Markdown rendering.  I want to build split screen editors that are smart and build off of ideas like GitHub's Jekyll.

#### Whitespace is informative

If it is a matter of compression, I just don't think there is real need.  Mobile networks are getting faster and the cloud keep on getting cheaper.  Why compress HTML?  Why loose any subtle amount of semantic data that could be hidden in the whitespace?  The main thing engineers need to worry about is the AMD JavaScript pattern that causes an excess of request cycles.  You should always compress your JavaScript into one file, that is the whole purpose of it's lexical make up.

#### No need for inline

There is no reasonable reason to extend Markdown to support the idea of inline Macros.  Outside of the agreed upon semantic features of writing itself nothing should need to exist inline with the text.

===

It's just a thought. Any consideration would be greatly appreciated!
