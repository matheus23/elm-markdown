# CommonMark - Raw HTML

## [Example 609](https://spec.commonmark.org/0.29/#example-609)

This markdown:

```markdown
<a><bab><c2c>

```

Should give output:

```html
<p><a><bab><c2c></p>
```

But instead was:

```html
ERROR Problem at row 2 Expecting symbol
```
## [Example 610](https://spec.commonmark.org/0.29/#example-610)

This markdown:

```markdown
<a/><b2/>

```

Should give output:

```html
<p><a><b2></p>
```

But instead was:

```html
ERROR Ran into a oneOf with no possibilities!
```
## [Example 611](https://spec.commonmark.org/0.29/#example-611)

This markdown:

```markdown
<a  /><b2
data="foo" >

```

Should give output:

```html
<p><a><b2 data="foo"></p>
```

But instead was:

```html
ERROR Problem at row 3 Expecting symbol
```
## [Example 612](https://spec.commonmark.org/0.29/#example-612)

This markdown:

```markdown
<a foo="bar" bam = 'baz <em>"</em>'
_boolean zoop:33=zoop:33 />

```

Should give output:

```html
<p><a _boolean="" bam="baz &lt;em&gt;&quot;&lt;/em&gt;" foo="bar" zoop:33="zoop:33"></p>
```

But instead was:

```html
ERROR Problem at row 2 Expecting symbol =
```
## [Example 613](https://spec.commonmark.org/0.29/#example-613)

This markdown:

```markdown
Foo <responsive-image src="foo.jpg" />

```

Should give output:

```html
<p>Foo<responsive-image src="foo.jpg"></p>
```

But instead was:

```html
<p>Foo &lt;responsive-image src=&quot;foo.jpg&quot; /&gt;</p>
```
## [Example 614](https://spec.commonmark.org/0.29/#example-614)

This markdown:

```markdown
<33> <__>

```

Should give output:

```html
<p>&lt;33&gt; &lt;__&gt;</p>
```

But instead was:

```html
ERROR Problem at row 2 Expecting symbol
```
## [Example 615](https://spec.commonmark.org/0.29/#example-615)

This markdown:

```markdown
<a h*#ref="hi">

```

Should give output:

```html
<p>&lt;a h*#ref=&quot;hi&quot;&gt;</p>
```

But instead was:

```html
ERROR Problem at row 2 Expecting symbol
```
## [Example 616](https://spec.commonmark.org/0.29/#example-616)

This markdown:

```markdown
<a href="hi'> <a href=hi'>

```

Should give output:

```html
<p>&lt;a href=&quot;hi&#39;&gt; &lt;a href=hi&#39;&gt;</p>
```

But instead was:

```html
ERROR Problem at row 2 Expecting symbol &quot;
```
## [Example 617](https://spec.commonmark.org/0.29/#example-617)

This markdown:

```markdown
< a><
foo><bar/ >
<foo bar=baz
bim!bop />

```

Should give output:

```html
<p>&lt; a&gt;&lt; foo&gt;&lt;bar/ &gt; &lt;foo bar=baz bim!bop /&gt;</p>
```

But instead was:

```html
ERROR Problem at row 1 Bad repeat
```
## [Example 618](https://spec.commonmark.org/0.29/#example-618)

This markdown:

```markdown
<a href='bar'title=title>

```

Should give output:

```html
<p>&lt;a href=&#39;bar&#39;title=title&gt;</p>
```

But instead was:

```html
ERROR Problem at row 1 Expecting symbol &quot; Problem at row 1 Expecting symbol &#39;
```
## [Example 619](https://spec.commonmark.org/0.29/#example-619)

This markdown:

```markdown
</a></foo >

```

Should give output:

```html
<p></a></foo></p>
```

But instead was:

```html
ERROR Problem at row 1 Bad repeat
```
## [Example 620](https://spec.commonmark.org/0.29/#example-620)

This markdown:

```markdown
</a href="foo">

```

Should give output:

```html
<p>&lt;/a href=&quot;foo&quot;&gt;</p>
```

But instead was:

```html
ERROR Problem at row 1 Bad repeat
```
## [Example 621](https://spec.commonmark.org/0.29/#example-621)

This markdown:

```markdown
foo <!-- this is a
comment - with hyphen -->

```

Should give output:

```html
<p>foo</p>
```

But instead was:

```html
<p>foo &lt;!-- this is a comment - with hyphen --&gt;</p>
```
## [Example 624](https://spec.commonmark.org/0.29/#example-624)

This markdown:

```markdown
foo <?php echo $a; ?>

```

Should give output:

```html
<p>foo</p>
```

But instead was:

```html
<p>foo &lt;?php echo $a; ?&gt;</p>
```
## [Example 625](https://spec.commonmark.org/0.29/#example-625)

This markdown:

```markdown
foo <!ELEMENT br EMPTY>

```

Should give output:

```html
<p>foo</p>
```

But instead was:

```html
<p>foo &lt;!ELEMENT br EMPTY&gt;</p>
```
## [Example 626](https://spec.commonmark.org/0.29/#example-626)

This markdown:

```markdown
foo <![CDATA[>&<]]>

```

Should give output:

```html
<p>foo&amp;&lt;]]&gt;</p>
```

But instead was:

```html
ERROR Problem at row 3 Expecting Problem at row 1 Expecting symbol (
```
## [Example 627](https://spec.commonmark.org/0.29/#example-627)

This markdown:

```markdown
foo <a href="&ouml;">

```

Should give output:

```html
<p>foo<a href="ö"></p>
```

But instead was:

```html
<p>foo &lt;a href=&quot;&amp;ouml;&quot;&gt;</p>
```
## [Example 628](https://spec.commonmark.org/0.29/#example-628)

This markdown:

```markdown
foo <a href="\*">

```

Should give output:

```html
<p>foo<a href="\*"></p>
```

But instead was:

```html
<p>foo &lt;a href=&quot;\<em>&quot;&gt;</em></p>
```
## [Example 629](https://spec.commonmark.org/0.29/#example-629)

This markdown:

```markdown
<a href="\"">

```

Should give output:

```html
<p>&lt;a href=&quot;&quot;&quot;&gt;</p>
```

But instead was:

```html
ERROR Problem at row 1 Expecting symbol /&gt; Problem at row 1 Expecting symbol &gt;
```
