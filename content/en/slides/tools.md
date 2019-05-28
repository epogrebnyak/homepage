+++
title = "Slides"

[slides]
# Choose a theme from https://github.com/hakimel/reveal.js#theming
theme = "white"  # Reveal JS theme name
highlight_style = "github"  # Highlight JS theme name
+++


# Userful tools and concepts

<https://epogrebnyak.github.io/slides/tools/>


---

# 1. Command line

If on Windows, install WSL.  
Go through [Art of command line](https://github.com/jlevy/the-art-of-command-line#basics>).

---

## Tasks

> Fluency on the command line is a skill often neglected or considered arcane, but it improves your flexibility and productivity as an engineer in both obvious and subtle ways. 

More at [Art of command line](https://github.com/jlevy/the-art-of-command-line#basics>).

---

## Concepts

  <!-- 
  - `~` vs `%USERPROFILE%`
  - `%PATH%` and `$PATH`
  -->

- file system (```~``` or ```%USERPROFILE%```, ```PATH```)
- streams and redirection (```>```, ```>>```, ```|```)
- args and flags ([docopt](http://docopt.org/))
- package managers (```apt-get```)

---

## Running on Windows 

  - [GOW](https://github.com/bmatzelle/gow/wiki)
  - Cygwin, MinGW
  - [Git for Windows](https://git-scm.com/downloads)
  - [cmder](https://cmder.net/)

---

## Windows Subsystem for Linux ([WSL](https://www.google.com/search?q=wsl))

<iframe width="560" height="315" src="https://www.youtube.com/embed/8gw0rXPMMPE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

Video: [WSL architecture](https://youtu.be/Zi0eofqAkXU?t=758)

---

## Remote machine 

[Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb#) is 
a free and fast way to play with command line on a remote machine.

---

## Example

```
apt-get tree
man tree
tree / -d -L 2
```

Why not try this in ​Google Colab?
Prefix every command with ```!```


---

## Cloud...
[![](https://fm.cnbc.com/applications/cnbc.com/resources/img/editorial/2014/07/16/101843014-sex-tape.530x298.jpg?v=1405549602)](https://www.cnbc.com/2014/07/17/using-sex-tape-to-explain-the-cloudcommentary.html)

---

## ... or just someone else's computer?

<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 

<center>
<blockquote class="twitter-tweet"><p lang="en" dir="ltr">&quot;Would you put your files on someone else&#39;s computer?&quot;<br><br>&quot;Lol no&quot;<br><br>&quot;Would you put your files in the cloud though?&quot;<br><br>&quot;That sounds lovely, I love clouds&quot;</p>&mdash; ᴠᴀɴ sᴄʜɴᴇɪᴅᴇʀ (@vanschneider) <a href="https://twitter.com/vanschneider/status/1029038916878385156?ref_src=twsrc%5Etfw">August 13, 2018</a></blockquote> 
</center>

---

## (Temp) free plans

<img class="plain"  src="/img/paycloud.png"/>

{{< speaker_note >}}

All have (temporarily) free plans:

{{< / speaker_note >}}

- [AWS EC2](https://aws.amazon.com/ru/ec2/)
- [Digital Ocean](https://www.digitalocean.com) 
- Yandex and Mail.ru

Tip: [Travis-CI artifacts](https://docs.travis-ci.com/user/uploading-artifacts/) 

---

## On mobile

[Termux (Android)](https://habr.com/ru/post/444950/)

<img class="plain"  src="https://termux.com/files/weechat-with-keyboard_framed.png"/>


---

# Test-driven development (TDD)

---

## Unit test, end-to-end tests and `dirty hybrids`

  - `UnitTest`
  - `pytest`

---

## Continious integration 

  - Travis CI
  - Circle CI

---

## Test coverage

---

# Git

- Use
- Concept
- Workflow 
- Work in small batches.

- Where:
  - Github
  - Gitlab

---

## Data

- Analysis is a DAG
- Data storage (AWS S3) 

---

## Publishing

- markdown, pandoc
- asciidoctor (Ruby)
- latex (Overleaf)
- doi, bibliography
- jekyll, hugo

---

Обеспечения надзора

- Руководитель экспертной группы
- Полонский

---

##  Coding

Tweet: coding interview

Concepts:

- OOP vs FP
- algorithm, O(n) notation
- Turing / state machine

Use:

- REPL + text editor
- databases: ORM, SQL
- regex

Learn from:

- SO
- dev.to
- library popularity on github

---

## Editors (vs IDEs)

- `:q`  for vim
- VSCode
- Sublime
- Notepad++ 

--- 

## Productivity

- todo.txt
- todos, try, doing, done
-  file naming

---

## Как вообще мы вызываем функцию?

<center>
<blockquote class="twitter-tweet">
<p lang="en" dir="ltr">f(5,6) - &quot;The ideal syntax for practical programmers&quot;<br>f 5 6 - &quot;Bizarre; only academics would use&quot;<br>(f 5 6) - &quot;Too many parentheses&quot;<br>5.f(6) - &quot;Preferred for your next web app&quot;</p>&mdash; Michael Burge (@TheMichaelBurge) <a href="https://twitter.com/TheMichaelBurge/status/1058885000588750848?ref_src=twsrc%5Etfw">November 4, 2018</a></blockquote> 

<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script> 
</center>

data-width=550

--- 

## A summary of

- <https://github.com/epogrebnyak/notes-linux-cli> for WSL
- <https://github.com/epogrebnyak/learn> for coding
- <https://github.com/epogrebnyak/notes-pandoc>
- <https://github.com/epogrebnyak/notes-slides>

---

Built with:

 - markdown 
 - Hugo
 - reveal.js
 - [Twitter search](https://www.unfollowspy.com/searchmy.php)

Tried: 
 - [gitpitch.com](http://gitpitch.com)

May try:
 - `npm reveal-md`

---

## Add Some Slide Candy

![](https://raw.githubusercontent.com/gitpitch/in-60-seconds/master/assets/img/presentation.png)

---
@title[Customize Slide Layout]

@snap[west span-50]
## Customize Slide Content Layout
@snapend

@snap[east span-50]
![](https://raw.githubusercontent.com/gitpitch/in-60-seconds/master/assets/img/presentation.png)
@snapend

---?color=#E58537
@title[Add A Little Imagination]

@snap[north-west]
#### Add a splash of @color[cyan](**color**) and you are ready to start presenting...
@snapend

@snap[west span-55]
@ul[spaced text-white]
- You will be amazed
- What you can achieve
- *With a little imagination...*
- And **GitPitch Markdown**
@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---?image=assets/img/presenter.jpg

@snap[north span-100 headline]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend


# Welcome to Slides

[Academic](https://sourcethemes.com/academic/)

---

## Features

- Efficiently write slides in Markdown
- 3-in-1: Create, Present, and Publish your slides
- Supports speaker notes
- Mobile friendly slides

---

## Controls

- Next: `Right Arrow` or `Space`
- Previous: `Left Arrow`
- Start: `Home`
- Finish: `End`
- Overview: `Esc`
- Speaker notes: `S`
- Fullscreen: `F`
- Zoom: `Alt + Click`
- [PDF Export](https://github.com/hakimel/reveal.js#pdf-export): `E`

---

## Code Highlighting

Inline code: `variable`

Code block:
```python
porridge = "blueberry"
if porridge == "blueberry":
    print("Eating...")
```

---

## Math

In-line math: $x + y = z$

Block math:

$$
f\left( x \right) = \;\frac{{2\left( {x + 4} \right)\left( {x - 4} \right)}}{{\left( {x + 4} \right)\left( {x + 1} \right)}}
$$

---

## Fragments

Make content appear incrementally

```
{{%/* fragment */%}} One {{%/* /fragment */%}}
{{%/* fragment */%}} **Two** {{%/* /fragment */%}}
{{%/* fragment */%}} Three {{%/* /fragment */%}}
```

Press `Space` to play!

{{% fragment %}} One {{% /fragment %}}
{{% fragment %}} **Two** {{% /fragment %}}
{{% fragment %}} Three {{% /fragment %}}

---

A fragment can accept two optional parameters:

- `class`: use a custom style (requires definition in custom CSS)
- `weight`: sets the order in which a fragment appears

---

## Speaker Notes

Add speaker notes to your presentation

```markdown
{{%/* speaker_note */%}}
- Only the speaker can read these notes
- Press `S` key to view
{{%/* /speaker_note */%}}
```

Press the `S` key to view the speaker notes!

{{< speaker_note >}}
- Only the speaker can read these notes
- Press `S` key to view
{{< /speaker_note >}}

---

## Themes

- black: Black background, white text, blue links (default)
- white: White background, black text, blue links
- league: Gray background, white text, blue links
- beige: Beige background, dark text, brown links
- sky: Blue background, thin dark text, blue links

---

- night: Black background, thick white text, orange links
- serif: Cappuccino background, gray text, brown links
- simple: White background, black text, blue links
- solarized: Cream-colored background, dark green text, blue links

---

{{< slide background-image="/img/boards.jpg" >}}

## Custom Slide

Customize the slide style and background

```markdown
{{</* slide background-image="/img/boards.jpg" */>}}
{{</* slide background-color="#0000FF" */>}}
{{</* slide class="my-style" */>}}
```

---

## Custom CSS Example

Let's make headers navy colored.

Create `assets/css/reveal_custom.css` with:

```css
.reveal section h1,
.reveal section h2,
.reveal section h3 {
  color: navy;
}
```

---

# Questions?

[Ask](https://discourse.gohugo.io)

[Documentation](https://sourcethemes.com/academic/docs/)
