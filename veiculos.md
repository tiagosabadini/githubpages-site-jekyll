---
layout: default
title: "Veículos disponíveis"
---

{%- if veiculos.size > 0 -%}
  <ul class="post-list">
    {%- for veiculo in veiculos -%}
    <li>
      <span class="post-meta">{{ post.date | date: date_format }}</span>
      <a class="post-link" href="{{ post.url | relative_url }}">
        {{ veiculo.title | escape }}
      </a>
      <p>Franquia: {{ veiculo.franschise }}</p>
      <p>Tempo do contrato: {{ veiculo.timeContract }}</p>
      <p>Valor da mensalidade: {{ veiculo.price }}</p>
      <img src="{{ veiculo.photo }}" width="322" />
      {%- if site.show_excerpts -%}
        {{ post.excerpt }}
      {%- endif -%}
    </li>
    {%- endfor -%}
  </ul>
{%- endif -%}