---
layout: default
title: "Veículos disponíveis"
---

{%- if site.posts.size > 0 -%}
  <ul class="post-list">
    {%- for post in site.posts -%}
      <li>
        <a class="post-link" href="{{ post.url | relative_url }}">
          {{ post.title | escape }}
        </a>
        <p>Categoria: {{ post.category }}</p>
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