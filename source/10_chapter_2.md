# The ML model {#sec:lit-review}

<!--
After the introductory chapter, it seems fairly common to
include a chapter that reviews the literature and
introduces methodology used throughout the thesis.
-->

## Structure of the model

Output von ARIMA


<!--
For italic, add _ on either side of the text
For bold, add ** on either side of the text
For bold and italic, add _** on either side of the text
-->

<!-- 

This is a brief outline of what went into each chapter, and a section which shows how to reference headers (which are labelled automatically for you). This chapter, @sec:intro, shows how to use citations and how to reference section headers. @sec:lit-review shows how use and reference equations. @sec:research-code shows how to use and reference code. @sec:research-figure shows how to use, reference, and resize pdf and jpg figures. @sec:research-table shows how to use and reference tables. @sec:research-final is truly revolutionary (but shows nothing functional). **[Appendix 1](#appendix-1-some-extra-stuff)** shows how to add chapters which are not numbered, and has to be referenced manually, as does **[Appendix 2](#appendix-2-some-more-extra-stuff)**. See the base [`README.md`](https://github.com/tompollard/phd_thesis_markdown/blob/master/README.md) for how References are handled - leave `*_references.md` alone, and provide it to `pandoc` last.

Proin faucibus nibh sit amet augue blandit varius.

This is the introduction. Duis in neque felis. In hac habitasse platea dictumst. Cras eget rutrum elit. Pellentesque tristique venenatis pellentesque. Cras eu dignissim quam, vel sodales felis. Vestibulum efficitur justo a nibh cursus eleifend. Integer ultrices lorem at nunc efficitur lobortis.

## The middle

This is the literature review. Nullam quam odio, volutpat ac ornare quis, vestibulum nec nulla. Aenean nec dapibus in mL/min^-1^. Mathematical formula can be inserted using Latex and can be automatically numbered:

$$f(x) = ax^3 + bx^2 + cx + d$$ {#eq:my_equation}

Nunc eleifend, ex a luctus porttitor, felis ex suscipit tellus, ut sollicitudin sapien purus in libero. Nulla blandit eget urna vel tempus. Praesent fringilla dui sapien, sit amet egestas leo sollicitudin at.

Later on in the text, you can reference [@eq:my_equation] and its mind-blowing ramifications. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Sed faucibus pulvinar volutpat. Ut semper fringilla erat non dapibus. Nunc vitae felis eget purus placerat finibus laoreet ut nibh.

## A complicated math equation
The following raw text in markdown behind [@eq:my_complicated_equation] shows that you can fall back on \LaTeX if it is more convenient for you. Note that this will only be rendered in `thesis.pdf`

$$
\begin{aligned}
    \hat{\theta}_g = \argmin_{\theta_g} \Big\{ - &\sum^{N}_{n=1}\Big( 1-\mathbb{1}[f(\pmb x^{(n)})]\Big)\log f\Big(\pmb x^{(n)} \\ 
    &+ g(\pmb x^{(n)};\theta_g)\Big) + \lambda|g(\pmb x^{(n)};\theta_g)|_2 \Big\} \ ,
\end{aligned}
$$ {#eq:my_complicated_equation}


## Conclusion

This is the conclusion. Donec pulvinar molestie urna eu faucibus. In tristique ut neque vel eleifend. Morbi ut massa vitae diam gravida iaculis. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.

<!-- Insert an unordered list -->

<!-- 

- first item in the list
- second item in the list
- third item in the list

<!-- 
Comments can be added like this.
--> 