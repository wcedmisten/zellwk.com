---
layout: post
title: New CSS Color syntax — rgb instead of rgba
slug: css-color-rgb-instead-of-rgba
tags: ['css', 'scss']
---

If you want to support transparency in a CSS `rgb` or `hsl` function, there's no need to write `rgba` or `hsla` anymore. You can simply write `rgb` or `hsl` with a `/` to indicate the alpha.

No need for commas too!

<!-- more -->

Here's an example.

```css
.rgb {
  rgb(59 50 103 / 0.3)
}

.hsl {
  color: hsl(250 35% 30% / 0.3);
}
```

Adam Argyle's tweet explains this better than I can.

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">rgb() ⇒ rgba() just to add transparency? 🤢<br>hsl() ⇒ hsla() ... 😭<br><br>GOOD NEWS!<br>fixed in CSS color-level-4,<br>rgb() &amp; hsl() accept a 4th parameter 🎉<br><br>color demo<a href="https://t.co/6uMtGvVbUY">https://t.co/6uMtGvVbUY</a><br><br>color level 4 docs<a href="https://t.co/T1PSfA6boS">https://t.co/T1PSfA6boS</a><br><br>🔥 tips<br>- try in your fav browser!<br>- drop comma&#39;s! <a href="https://t.co/xjc3DrPG0A">pic.twitter.com/xjc3DrPG0A</a></p>&mdash; Adam Argyle (@argyleink) <a href="https://twitter.com/argyleink/status/1218305696862588928?ref_src=twsrc%5Etfw">January 17, 2020</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

Here's the good news: **This is supported across all major browsers** — so you can use it in production today!

You can also use this if you're a Sass user — **Dart Sass supports this syntax too**, but it converts the function into a regular `rgba` underneath the hood.

```scss
// What you write
.selector {
  color: hsl(250 35% 30% / 0.3);
}

// Compiled CSS
.selector {
  color: rgba(59, 50, 103, 0.3);
}
```

That's it!
