---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
list_title: Neuigkeiten
---
<div class="category-listing">
  {%- if page.title -%}
    <h1 class="page-heading">{{ page.title }}</h1>
  {%- endif -%}

  {%- if site.tags.size > 0 -%}
  {% for tag in site.tags %}
    <section class="category" id="{{ tag[0] | slugify:'latin' }}">
	<h2 class="post-list-heading">Alle Seiten mit Schlagwort „{{ tag[0] }}“</h2>
    <ul class="post-list">
      {%- for post in tag[1] -%}
  	    {% include post-preview.html %}
      {%- endfor -%}
    </ul>
	</section>
  {% endfor %}
  {%- endif -%}

</div>
