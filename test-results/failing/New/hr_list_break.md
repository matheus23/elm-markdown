# New - hr_list_break

## Example undefined

This markdown:

```markdown
* hello
world
* how
are
* * *
you today?

```

Should give output:

```html
<ul><li>hello world</li><li>how are</li></ul><hr><p>you today?</p>
```

But instead was:

```html
<ul><li><p>hello</p></li></ul><p>world</p><ul><li><p>how</p></li></ul><p>are</p><ul><li><p><em></em></p></li></ul><p>you today?</p>
```
