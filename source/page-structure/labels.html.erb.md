---
title: Labeling Regions
order: 3
wcag_success_criteria:
  - 2.4.1
  - 2.4.6
wcag_techniques:
  - H69
  - ARIA11
technologies: HTML5, WAI-ARIA
editors:
- Eric Eggert: "https://www.w3.org/People/yatil/"
- Shadi Abou-Zahra: "https://www.w3.org/People/shadi/"
contributors:
- The Education and Outreach Working Group (<a href="https://www.w3.org/WAI/EO/">EOWG</a>)
support: Developed with support from the <a href="https://www.w3.org/WAI/ACT/">WAI-ACT project</a>, co-funded by the <strong>European Commission <abbr title="Information Society Technologies">IST</abbr> Programme</strong>.
---
Most regions on a page should be labeled. Labels are especially important when multiple regions of the same type are on one page, such as multiple navigation options. WAI-ARIA provides simple mechanisms for labeling a region, enabling users to navigate around the page quickly.

Sections should also be organized using [headings](headings.html).

## Using `aria-label`
{:.ap}

{::nomarkdown}
<%= ref :start %>
{:/nomarkdown}

Use the WAI-ARIA `aria-label` attribute to label the region. Consider this approach if the label should not appear visually on the page.

{::nomarkdown}
<%= ref :middle %>
{:/nomarkdown}

Explore other WAI-ARIA resources:

* [WAI-ARIA Overview](https://www.w3.org/WAI/intro/aria)
* [Notes on Using ARIA in HTML](https://www.w3.org/TR/aria-in-html/)

{::nomarkdown}
<%= ref :end %>
{:/nomarkdown}

{::nomarkdown}
<%= demo :start %>
{:/nomarkdown}

{::nomarkdown}
<%= code_start %>
{:/nomarkdown}

~~~html
<nav aria-label="Main Navigation">
  …
</nav>
~~~

{::nomarkdown}
<%= code_end %>
{:/nomarkdown}

{::nomarkdown}
<%= demo :middle %>
{:/}

View a [complete code example](example.html) with regions and labels.

{::nomarkdown}
<%= demo :end %>
{:/}

## Using `aria-labelledby`
{:.ap}

Use the WAI-ARIA `aria-labelledby` to reference an existing element – like a heading – by its (unique) `id`. The content of the referenced element is then used as the label. A heading allows users to find the region in multiple ways.

{::nomarkdown}
<%= code_start %>
{:/nomarkdown}

~~~html
<nav aria-labelledby="regionheading">
  <h3 id="regionheading">On this Page</h3>
    …
</nav>
~~~

{::nomarkdown}
<%= code_end %>
{:/nomarkdown}
