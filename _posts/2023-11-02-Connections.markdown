---
layout: post
title: "A note about connections"
date: 2023-11-02 
categories: jekyll update
---

### Introduction

In multivariable calculus, one often takes directional derivatives of vector fields with respect to other vector fields. How can one do this on a manifold? $\nabla_X Y$

<!-- Need to use double backslash square bracket. Setting displayMath: [['\[', '\]']] in default.html 
correctly made it so that \[ and \] would delimit displayed math, but then it would read any square
brackets inside the delimiters as a delimiter itself. Of course, escaping didn't work.
-->
\\[
R(X,Y)Z = [\nabla_X, \nabla_Y]Z - \nabla_{[X, Y]}Z.  
\\]


<!--
DEFAULT JEKYLL STUFF
CAN IGNORE, BUT LEAVING IT IN INCASE IT'S USEFUL

`YEAR-MONTH-DAY-title.MARKUP`

Where `YEAR` is a four-digit number, `MONTH` and `DAY` are both two-digit numbers, and `MARKUP` is the file extension representing the format used in the file. After that, include the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
-->
