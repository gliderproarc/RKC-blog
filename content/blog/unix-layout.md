+++
title = "Org-mode table allignment with non-latin characters"
author = ["Robert Clay"]
date = 2021-02-06
lastmod = 2021-02-04T20:10:23+09:00
categories = ["topic"]
draft = true
+++

<span class="timestamp-wrapper"><span class="timestamp">[2021-01-30 Sat]</span></span>,#org-mode


## Org-mode tip {#org-mode-tip}

This article won't mean much if you don't use or intent to use Org-mode, and it
means even less for you if you only write in a language that uses latin
characters. But if you do write things like おそれいれますが or 可能性 AND you
want to put them in an Org mode table, then this is for you.

I was using Org mode for a table at work, and I noticed that the alignment was
off when Japanese characters were present in the table.

\*you need to view this in a mono-space font for it to look right but here goes

```text
| Name | Age |
|------+-----|
| Bill |   3 |
| Ann  |  30 |
| John |  78 |
```

That looks just fine, but you might see some alignment errors depending on your
font for this next table

```text
| 名前       | 年齢 |
|------------+------|
| ジョ       |    4 |
| ココロ     |   29 |
| ハビエルア |   43 |
```

If that doesn't make a nice square, you might have a font that doesn't have a
proper mono-space size for these asian characters. But there is hope for Emacs
users. Emacs let's you set all kinds of things. Once of them is the face for
fonts used in various places in Emacs. If you are using Doom Emacs, you can
include something like this in your ".config.el":
