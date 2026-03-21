<h2 id="publications" style="margin: 2px 0px -15px;">Papers</h2>

<div class="publications">
<ol class="bibliography">
{% for link in site.data.publications.main %}
<li style="margin-bottom: 15px;">
<div class="pub-row" style="display: flex; min-height: auto">
  <!-- <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;align-self: flex-start;">
    {% if link.image %} 
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
    {% if link.journal_short %} 
    <abbr class="badge">{{ link.journal_short }}</abbr>
    {% endif %}
    {% endif %}
  </div> -->
  <!-- <div class="col-sm-1" style="align-self: flex-start; text-align: right; padding-right: 15px; font-weight: bold; color: #555;"> -->
  <div style="flex: 0 0 50px; align-self: flex-start; text-align: center; font-weight: bold; color: #555;">
    [{{ forloop.rindex }}]
  </div>
  <!-- <div class="col-sm-11" style="position: relative;padding-right: 15px;padding-left: 20px;align-self: flex-start;"> -->
  <div style="flex: 1; position: relative; padding-right: 15px; padding-left: 10px; align-self: flex-start;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.journal }}</em>
      </div>
    <div class="links">
      {% if link.abstract %} 
      <a class="btn btn-sm z-depth-0" role="button" style="font-size:12px; cursor: pointer;" onclick="var el = document.getElementById('abs-{{ link.title | slugify }}'); el.style.display = (el.style.display === 'none') ? 'block' : 'none';">abstract</a>
      {% endif %}
      {% if link.arXiv %} 
      <a href="{{ link.arXiv }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">arXiv</a>
      {% endif %}
      {% if link.doi %} 
      <a href="{{ link.doi }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">DOI</a>
      {% endif %}
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.undergrad %} 
      <span style="color: #6c757d; font-style: italic;">(undergraduate research)</span>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
    {% if link.abstract %}
      <div id="abs-{{ link.title | slugify }}" style="display: none; margin-top: 10px; padding: 12px; background-color: #f8f9fa; border-left: 3px solid #6c757d; font-size: 13px; line-height: 1.5; border-radius: 0 4px 4px 0;">
        {{ link.abstract }}
      </div>
    {% endif %}
  </div>
</div>
</li>
{% endfor %}
</ol>
</div>
