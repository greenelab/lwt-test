---
title: Demo
---

# <i class="fa-solid fa-vials"></i>Demo

A demo of the template's Markdown formatting and built-in components.

{% include section.html %}

## Basic Formatting

_italic text_

**bold text**

~~strike-through text~~

<br>
<br>
Text with extra blank lines above and below
<br>
<br>
 
- list item a
- list item b
- list item c
 
1. ordered list item 1
2. ordered list item 2
3. ordered list item 3
 
[External link](https://some-website.org/)
 
[Internal link](team)
 
Centered free text
{:.center}
 
Horizontal rule:
 
---
 
| TABLE | Game 1 | Game 2 | Game 3 | Total |
| :---- | :----: | :----: | :----: | ----: |
| Anna  |  144   |  123   |  218   |   485 |
| Bill  |   90   |  175   |  120   |   385 |
| Cara  |  102   |  214   |  233   |   549 |
 
> It was the best of times it was the worst of times.
> It was the age of wisdom, it was the age of foolishness.
> It was the spring of hope, it was the winter of despair.
 
```javascript
// some code with syntax highlighting
const popup = document.querySelector("#popup");
popup.style.width = "100%";
popup.innerText =
  "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.";
```
 
This sentence has `inline code`, useful for making references to variables, packages, versions, etc. within a sentence.
 
Font Awesome icons:
<i class="fas fa-flask"></i>
<i class="fas fa-microscope"></i>
<i class="fas fa-bacteria"></i>
<i class="fas fa-virus"></i>
 
{% include section.html %}
 
## Components
 
{% include section.html %}
 
### Section
 
{%
  include section.html
  dark=false
  full=false
%}
 
Section, `dark=false`
 
{%
  include section.html
  dark=true
  full=false
%}
 
Section, `dark=true`
 
{% include section.html background="images/banner.jpg" %}
 
Section, `background` `dark=false`
 
{% include section.html background="images/banner.jpg" dark=true %}
 
Section, `background` `dark=true`
 
{% include section.html %}
 
### Banner
 
{% include section.html full=true %}
 
{% include banner.html image="images/banner.jpg" %}
 
{% include section.html %}
 
### Figure
 
{%
  include figure.html
  image="images/photo.jpg"
  caption="Figure with caption, link, and `px` width"
  link="team"
  width="400px"
%}
 
{%
  include figure.html
  image="images/photo.jpg"
  caption="Figure with caption, link, and `%` width"
  link="team"
  width="50%"
%}
 
{%
  include figure.html
  image="images/photo.jpg"
  caption="Figure with caption, link, and `px` height"
  link="team"
  height="200px"
%}
 
{% include section.html %}
 
### Gallery
 
{%
  include gallery.html
  image1="images/photo.jpg"
  link1="https://greenelab.com/"
  tooltip1="Image 1"
  image2="images/member.jpg"
  link2="https://greenelab.com/"
  image3="images/photo.jpg"
%}
 
{%
  include gallery.html
  image1="images/photo.jpg"
  link1="https://greenelab.com/"
  tooltip1="Image 1"
  image2="images/member.jpg"
  link2="https://greenelab.com/"
  image3="images/photo.jpg"
  style="square"
%}
 
{% include section.html %}
 
### Feature
 
{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Regular feature"
  text="Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat."
%}
 
{% capture text %}
Any kind of _component_ or **markdown**.
{:.center}
{% endcapture %}
 
{%
  include feature.html
  image="images/photo.jpg"
  link="team"
  title="Feature with arbitrary content"
  text=text
  flip=true
%}
 
{% include section.html %}
 
### Link
 
{%
  include link.html
  type="twitter"
  icon=""
  text=""
  tooltip=""
  link=""
%}
{%
  include link.html
  type="twitter"
  icon=""
  text=""
  tooltip=""
  link=""
  style="button"
%}
{%
  include link.html
  type="home-page"
  icon=""
  text="My Homepage"
  tooltip="My cool website"
  link=""
%}
{%
  include link.html
  type="home-page"
  icon=""
  text="My Homepage"
  tooltip="My cool website"
  link=""
  style="button"
%}
{:.center}
 
{% include section.html %}
 
### List
 
List team members, using the portrait component, with no `group` first, then list ones with `group` equal to `alum`, using a smaller portrait.
 
{% include list.html data="members" component="portrait" filters="group: " %}
 
{% include list.html data="members" component="portrait" filters="group: alum" style="small" %}
 
List citations, using the citation component, with `date` containing `2020`.
 
{%
  include list.html
  data="citations"
  component="citation"
  filters="date: ~2020"
%}
 
{% include section.html %}
 
### Card
 
{%
  include card.html
  image="images/photo.jpg"
  link="https://nasa.gov/"
  title="A Large Card"
  subtitle="A cool card"
  description="A cool description"
  tooltip="A cool tooltip"
  tags="manual tag"
  repo="greenelab/lab-website-template"
%}
 
{%
  include card.html
  image="images/photo.jpg"
  link="https://nasa.gov/"
  title="A Small Card"
  subtitle="A cool card"
  description="A cool description"
  tooltip="A cool tooltip"
  tags="manual tag"
  repo="greenelab/lab-website-template"
  style="small"
%}
 
{% include section.html %}
 
### Citation
 
Citation looked up by id.
 
{%
  include citation.html
  lookup="doi:10.1016/j.csbj.2020.05.017"
%}
 
Citation looked up by title, and with rich styling.
 
{%
  include citation.html
  lookup="Constructing knowledge graphs"
  style="rich"
%}
 
{% include section.html %}
 
### Tags
 
{%
  include tags.html
  tags="ovarian cancer, dataset, gene expression"
  repo="greenelab/lab-website-template"
  link="blog"
%}
 
{% include section.html %}
 
### Portrait
 
{%
  include portrait.html
  id="felix-cited"
%}
 
{% include section.html %}
 
### Role
 
{%
  include role.html
  type="pi"
  description="Senior Researcher"
  text=true
%}
{%
  include role.html
  type="phd"
  text=true
%}
{%
  include role.html
  type="programmer"
%}
 
{% include section.html %}
 
### Two Col
 
{% capture col1content %}
{% include figure.html image="images/photo.jpg" caption="Fig. 1a" %}
Lorem _ipsum_ dolor **sit** amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
{% endcapture %}
{% capture col2content %}
{% include figure.html image="images/photo.jpg" caption="Fig. 1b" %}
Lorem _ipsum_ dolor **sit** amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
{% endcapture %}
 
{% include two-col.html col1=col1content col2=col2content %}
 
{% include section.html %}
 
### Post Excerpt
 
{%
  include post-excerpt.html
  id="example-post-1"
%}
 
{% include section.html %}
 
### Search
 
{% include search-box.html %}
 
{% include search-info.html %}
 
{% include section.html %}
 
### Site Search
 
{% include site-search.html %}
 
{% include section.html %}
 
### Embeds
 
<a class="twitter-timeline center" data-height="400" href="https://twitter.com/GreeneScientist?ref_src=twsrc%5Etfw">Tweets by GreeneScientist</a> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
