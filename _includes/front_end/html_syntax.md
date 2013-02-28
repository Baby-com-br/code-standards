### Syntax


#### HTML5, please

We do not want to be stuck in the past, so we are using `<!DOCTYPE html5>`. Also,
use the short-handed versions of some properties, such as:

{% highlight html %}
<!-- Old -->
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8" />
<script type="text/javascript">

<!-- New -->
<meta charset="utf-8" />
<script>
{% endhighlight %}


#### Basics

These are the basic rules when writing HTML:

##### Identation: 2 spaces

{% highlight html %}
<!-- WRONG -->
<div class="foo">
    <div class="bar">
        <p>Yeah</p>
    </div>
</div>

<!-- CORRECT -->
<div class="foo">
  <div class="bar">
    <p>Yeah</p>
  </div>
</div>
{% endhighlight %}


##### Lowercase only

{% highlight html %}
<!-- WRONG -->
<UL>
  <LI CLASS="foo">Item 1</LI>
</UL>

<!-- CORRECT -->
<ul>
  <li class="foo">Item 1</li>
</ul>
{% endhighlight %}


##### Double quotes all the way

{% highlight html %}
<!-- WRONG -->
<p id="mixed" class='feelings'>

<!-- CORRECT -->
<p id="mixed" class="feelings">
{% endhighlight %}


#### XHTML-ish

In order to maintain a single, consistent standard across the application,
we use the XHTML syntax, which means:


##### Close self-contained tags

{% highlight html %}
<!-- WRONG -->
<img src="happy_cat.jpg" alt="Happy cat!">

<!-- CORRECT -->
<img src="happy_cat.jpg" alt="Happy cat!" />
{% endhighlight %}


##### Quoted attribute values

{% highlight html %}
<!-- WRONG -->
<img src=happy_cat.jpg />

<!-- CORRECT -->
<img src="happy_cat.jpg" />
{% endhighlight %}


##### Close all tags (even the optionals)

{% highlight html %}
<!-- WRONG -->
<p>Look at this list:

<ul>
  <li>Item 1
  <li>Item 2
</ul>

<!-- CORRECT -->
<p>Look at this list:</p>

<ul>
  <li>Item 1</li>
  <li>Item 2</li>
</ul>
{% endhighlight %}