# GFM - [extension] Task list items

## [Example 279](https://github.github.com/gfm/#example-279)

This markdown:

```markdown
- [ ] foo
- [x] bar
```

Should give output:

```html
<ul><li><input disabled="" type="checkbox">foo</li><li><input checked="" disabled="" type="checkbox">bar</li></ul>
```

But instead was:

```html
ERROR Problem at row 3 Expecting symbol
```
## [Example 280](https://github.github.com/gfm/#example-280)

This markdown:

```markdown
- [x] foo
  - [ ] bar
  - [x] baz
- [ ] bim
```

Should give output:

```html
<ul><li><input checked="" disabled="" type="checkbox">foo<ul><li><input disabled="" type="checkbox">bar</li><li><input checked="" disabled="" type="checkbox">baz</li></ul></li><li><input disabled="" type="checkbox">bim</li></ul>
```

But instead was:

```html
ERROR Problem at row 3 Expecting --- Problem at row 3 Expecting *** Problem at row 3 Expecting ___
```
