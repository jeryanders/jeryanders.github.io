---
# I need Jekyll to parse and render my resume from markdown form to
# convert it to html, but it only renders files that include their
# Front Matter configuration. The downside to this is that if
# anyone wants to view the resume in markdown format, the front
# matter is displayed as well. That isn't very clean looking, so
# I want to avoid it. I can't seem to find a way to easily get
# Jekyll to parse files that don't have front matter, so this
# file is the solution.
#
# I write my resume in markdown format like I want, and then
# include that markdown file into this one using Jekyll's
# include system. That way the resume file stays clean, and
# this file is what triggers the render (which works nicely
# anyway, since we want index to be the primary page, and
# the resume can have the nice, clear resume name).

# Use the resume layout as our html template.
layout: "resume"
---
{% capture resume %}{% include resume.md %}{% endcapture %}
{{ resume | markdownify }}
