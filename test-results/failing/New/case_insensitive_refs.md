# New - case_insensitive_refs

## Example undefined

This markdown:

```markdown
[hi]

[HI]: /url

```

Should give output:

```html
<p><a href="/url">hi</a></p>
```

But instead was:

```html
ERROR Problem at row 6 Expecting Problem at row 1 Expecting symbol (
```
