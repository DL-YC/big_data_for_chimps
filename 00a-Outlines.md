

* ready to go to tech review
* sections are filled out, TODOs are done
  - they'll make comments, but those don't need to be handled til later
* doesn't have to be perfect


* Tie each chapter to the goals of the book
  - ...
  - ...
  - ...


Introduce the chapter to the reader
* take the strands from the last chapter, and show them braided together
* in this chapter, you'll learn .... OR ok we're done looking at that, now let's xxx
* weave in the locality question


## Geographic data

Continuous horizon: getting 1-d locality

## Statistics

Data is worthless. Actually, it's worse than worthless. It costs you money to gather, store, manage, replicate and analyze. What you really want is insight -- a relevant summary of the essential patterns in that data -- produced using relationships to analyze data in context.

Statistical summaries are the purest form of this activity, and will be used repeatedly in the book to come, so now that you see how Hadoop is used it's a good place to focus.

Some statistical measures let you summarize the whole from summaries of the parts: I can count all the votes in the state by summing the votes from each county, and the votes in each county by summing the votes at each polling station. Those types of aggregations -- average/standard deviation, correlation, and so forth -- are naturally scalable, but just having billions of objects introduces some practical problems you need to avoid. We'll also use them to introduce Pig, a high-level language for SQL-like queries on large datasets.

Other statistical summaries require assembling context that grows with the size of the whole dataset. The amount of intermediate data required to count distinct objects, extract an accurate histogram, or find the median and other quantiles can become costly and cumbersome. That's especially unfortunate because so much data at large scale has a long-tail, not normal (Gaussian) distribution -- the median is far more robust indicator of the "typical" value than the average. (If Bill Gates walks into a bar, everyone in there is a billionaire on average.)

But you don't always need an exact value -- you need actionable insight. There's a clever pattern for approximating the whole by combining carefully re-mixed summaries of the parts, and we'll apply it to

* Holistic vs algebraic aggregations
* Underflow and the "Law of Huge Numbers"
* Approximate holistic aggs: Median vs remedian; percentile; count distinct (hyperloglog)
* Count-min sketch for most frequent elements
* Approx histogram

## Storm+Trident



* Routing primitives: Batch persist, Batch foreach, group persistent aggregate,

## Locality

* Understand relativity: horizons of belief, computation, delay, etc
* How guarantees of bounded disorder or delay, uniform sampling, etc let you trade off
* Aggregation types: holistic, algebraic, combinable; accumulate, accretion