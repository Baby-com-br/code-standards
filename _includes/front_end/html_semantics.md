### Semantics

#### Basics




#### New HTML5 authoring tags

Feel free to use the new block and inline level tags from the HTML5 spec.
Just remember a few rules about them, specific to our applications:

* `<section>`: Defines the main section of a document, and the subsections
  inside the section. Rule of thumb: it must have a related header tag (`h1`,
  `h2` etc.)
* `<article>`: The content of it must be self contained element that may be
  syndicated (like on a RSS feed or JSON document). Examples: a blog post,
  a product, a tweet.
* `<footer>`: It may be used for purposes other than the site's footer.
  The mini-cart's portion with total quantity and value is a `<footer>`, for
  example. And yes, it doesn't have to be the last child of a block.
* `<header>`: Just like the `<footer>`, it doesn't have to be restricted to
  the site's header. A product's header, for example, may contain its title
  and brand.
* `<nav>`: It's a navigation element. It doesn't have to be just the site's
  menu. However, remember it is a sectioning element, so it should have a related
  header tag—even a visually hidden one.

Read more about them [here](http://www.w3.org/TR/html5/)


#### Forms

Forms do not have a single, exact way to be authored, so here's the pattern
we use in order to keep a standard format:

{% highlight html %}
<!--
  We use novalidate because it's still a bit unstable, and we rely on
  JavaScript to display the correct message and format
-->
<form novalidate>
  <div class="input-field">
    <label for="foo">Foo</label>
    <input type="text" id="foo" />
  </div>

  <div class="input-field">
    <label for="foo-with-error">Field with error</label>
    <input type="text" id="foo-with-error" class="field-error" />

    <div class="invalid-input-field" style="">
      <p for="foo-with-error" generated="true" class="field-error">
        Error message
      </p>
    </div>
  </div>

  <div class="state-select input-field">
    <label for="address-state">Estado</label>
    <select id="address-state">
      <option value=""></option>
      <option value="SP">SP</option>
    </select>
  </div>

  <div class="submit">
    <input type="submit" value="Go!" />
  </div>
</form>
{% endhighlight %}

And if the form has multiple sections, always use `<fieldset>`.

{% highlight html %}
<!--
  We use novalidate because it's still a bit unstable, and we rely on
  JavaScript to display the correct message and format
-->
<form novalidate>
  <fieldset>
    <h3>Describe your foo</h3>

    <div class="input-field">
      <label for="foo">Foo</label>
      <input type="text" id="foo" />
    </div>
  </fieldset>

  <fieldset>
    <h3>Describe your bar</h3>

    <div class="input-field">
      <label for="bar">Bar</label>
      <input type="text" id="bar" />
    </div>
  </fieldset>

  <div class="submit">
    <input type="submit" value="Go!" />
  </div>
</form>
{% endhighlight %}