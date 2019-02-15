# 用R Markdown创建文档


+ Blog
    - [blogdown](https://github.com/rstudio/blogdown)
+ Book
    - [bookdown](https://github.com/rstudio/bookdown)
	- [bookdown](https://bookdown.org/yihui/bookdown/)
+ CV
    - [vitae](https://github.com/ropenscilabs/vitae)
+ Document
    - [rmarkdown](https://github.com/rstudio/rmarkdown)
+ Poster
    - [posterdown](https://github.com/brentthorne/posterdown) 

# R Markdown Tutorial
+ Tutorial:<http://www.jacolienvanrij.com/Tutorials/tutorialMarkdown.html>, <https://ourcodingclub.github.io/2016/11/24/rmarkdown-1.html>

# R Markdown questions
+ <https://stackoverflow.com/questions/20303826/highlight-bash-shell-code-in-markdown>
+ <https://stackoverflow.com/questions/25104738/text-highlight-in-markdown>

# Writing Mathematic in R Markdown 
+ <http://csrgxtu.github.io/2015/03/20/Writing-Mathematic-Fomulars-in-Markdown/>
+ <https://github.com/goessner/mdmath>
 ## Example
 ```
 $$ c^2 = a^2 + b^2 $$
 ```
 > $$ c^2 = a^2 + b^2 $$
 
 ```
 $ c = \sqrt{a^2+b^2} $
 ```
 > $`c = \sqrt{a^2 + b ^2}`$

 ```
 $$ 
 M = \left( \begin{array}{ccc}
 x_{11} & x_{12} $ \ldots \\
 x_{21} & x_{22} $ \ldots \\
 \vdots & \vdots $ \ldots \\
 \end{array} \right)
 $$
 ```
 > $$ 
 M = \left(\begin{array}{ccc} x_{11} & x_{12} & \ldots \\x_{21} & x_{22} & \ldots \\ \vdots & \vdots & \ldots \\ \end{array} \right)
 $$

 ```
 $$ h_{\theta} = \theta_{0}x + \theta_{1}x \tag{1}\label{eq:test} $$
 Referring to Eq. $\eqref{eq:test}$.
 ```
 > $$\begin{equation} h_{\theta} = \theta_{0}x + \theta_{1}x \tag{1}\label{eq:test} \end{equation}$$
 
 Referring to Eq. $\eqref{eq:test}$.


