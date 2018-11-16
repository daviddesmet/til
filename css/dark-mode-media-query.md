# Detect whether the user has Dark Mode enabled

With the introduction of [dark mode in macOS](https://developer.apple.com/design/human-interface-guidelines/macos/visual-design/dark-mode/), [Safari Technology Preview](https://developer.apple.com/safari/technology-preview/) 68 has released a new feature called `prefers-color-scheme` which lets us detect whether the user has dark mode enabled with a media query.

Here's an example:

```css
:root {
  --body-bg: #fafafa;
  --body-color: #555;
  --link-color: #222;
  --link-color-hover: #000;
}
@media (prefers-color-scheme: dark) {
  :root {
    --body-bg: #212529;
    --body-color: #6c757d;
    --link-color: #dee2e6;
    --link-color-hover: #fff;
  }
}
```

Another example by **Mark Otto** showing how he uses it on his own website to adjust images so that they’re comfortable while reading at night:

```css
@media (prefers-color-scheme: dark) {
  img {
    opacity: .75;
    transition: opacity .5s ease-in-out;
  }
  img:hover {
    opacity: 1;
  }
}
```

See [prefers-color-scheme](https://drafts.csswg.org/mediaqueries-5/#prefers-color-scheme) for more details.
[Source](http://markdotto.com/2018/11/05/css-dark-mode/)