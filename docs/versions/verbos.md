---
layout: default
title: Verbos - Spanish
parent: How to...
nav_order: 2
---
<h2>Verbos</h2>

{% for row in site.how_to_rows %}
{{row.content | replace: "xx-product-xx", "Verbos"}}

{%- if row.screenshot %}
{% capture iphoneStr %} {{"/assets/images/verbos/iPhone/"| prepend: site.baseurl | prepend: site.url}}{{ row.screenshot  }}.png {% endcapture %}
{% capture ipadStr %} {{"/assets/images/verbos/iPad/"| prepend: site.baseurl | prepend: site.url}}{{ row.screenshot  }}.png {% endcapture %}
<table>
<tbody>
	<tr>
		<td class = "iphone">
			<figure >
				<img class="iphone"  src="{{ iphoneStr }}" alt="Image" />
			</figure>
		</td>
		<td  class = "ipad">
			<figure>
				<img class="ipad"  src="{{ ipadStr }}" alt="Image" />
			</figure>
		</td>
	</tr>
</tbody>
</table>
{%- endif -%}

{% endfor %}


