---
layout: default
title: "Veículos disponíveis"
---

{%- if site.posts.size > 0 -%}
  <ul class="post-list">
    {{ assign filtered_posts = site.posts | where_exp:"item", "item.category == suv" }}
    {%- for post in filtered_posts -%}
    <li>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ post.title | escape }}
      </a>
      <p>Franquia: {{ post.franschise }}</p>
      <p>Tempo do contrato: {{ post.timeContract }}</p>
      <p>Valor da mensalidade: {{ post.price }}</p>
      <img src="{{ post.photo }}" width="322" />
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>
{%- endif -%}