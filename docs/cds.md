---
title: "CDs - Le Site Web de Suika AKIYAMA"
title_for_header: "CDs"
description: "CDリスト"
---
<div>
{% assign doclist = site.pages | sort: 'url' | reverse %}
  {% for doc in doclist %}
    {% if doc.url contains 'cds/' %}
      <style>
        @media screen and (min-width:450px){
          #{{ doc.name | remove: '.md' }}_jacket_b:checked ~ img.cds-first-image {
            width:0%;
            transition: all 1s;
            position: absolute;
          }
          #{{ doc.name | remove: '.md' }}_jacket_c:checked ~ img.cds-first-image {
            width:0%;
            transition: all 1s;
            position: absolute;
          }
          #{{ doc.name | remove: '.md' }}_jacket_c:checked ~ .cds-third-image {
            width:0%;
            transition: all 1s;
            position: absolute;
            transition-delay: 0.5s;
          }
          #{{ doc.name | remove: '.md' }}_jacket_c:checked ~ .cds-second-image {
            transform: rotate(720deg);
            transition: all 1.5s;
            transition-delay: 1s;
          }
        }
        @media screen and (max-width:450px){
          #{{ doc.name | remove: '.md' }}_jacket_b:checked ~ img.cds-first-image {
            opacity: 0;
            transition: all 1s;
            position: absolute;
          }
          #{{ doc.name | remove: '.md' }}_jacket_c:checked ~ img.cds-first-image {
            opacity: 0;
            transition: all 1s;
            position: absolute;
          }
          #{{ doc.name | remove: '.md' }}_jacket_c:checked ~ .cds-third-image {
            opacity: 0;
            transition: all 1s;
            position: absolute;
            transition-delay: 0.5s;
          }
          #{{ doc.name | remove: '.md' }}_jacket_c:checked ~ .cds-second-image {
            transform: rotate(720deg);
            transition: all 1.5s;
            transition-delay: 1s;
          }
        }
      </style>
      <h3 id="{{ doc.title }}">{{ doc.title }}</h3>
      <div class="song-block">
        <div class="cds-float-left">
          <input type="radio" name="{{ doc.name | remove: '.md' }}_select" id="{{ doc.name | remove: '.md' }}_jacket_a" class="non" checked>
          <input type="radio" name="{{ doc.name | remove: '.md' }}_select" id="{{ doc.name | remove: '.md' }}_jacket_b" class="non">
          <input type="radio" name="{{ doc.name | remove: '.md' }}_select" id="{{ doc.name | remove: '.md' }}_jacket_c" class="non">
          <img src="https://sueakiyama.github.io/cds/images/{{ doc.name | remove: '.md' }}_a.webp" alt="ジャケット" class="cds-first-image cds-images">
          <img src="https://sueakiyama.github.io/cds/images/{{ doc.name | remove: '.md' }}_c.webp" alt="レーベル" class="cds-second-image cds-images">
          <img src="https://sueakiyama.github.io/cds/images/{{ doc.name | remove: '.md' }}_b.webp" alt="ジャケット裏" class="cds-third-image cds-images">
        </div>
        <table class="cds-float-right">
          <thead>
            <tr>
              <th>タイトル</th>
              <th>{{ doc.title }}</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td>画像</td>
              <td>
                <label for="{{ doc.name | remove: '.md' }}_jacket_a"><a>ジャケット表面</a></label>・
                <label for="{{ doc.name | remove: '.md' }}_jacket_b"><a>ジャケット裏面</a></label>・
                <label for="{{ doc.name | remove: '.md' }}_jacket_c"><a>レーベル</a></label>
              </td>
            </tr>
            <tr>
              <td>価格</td>
              <td>{{ doc.price }}</td>
            </tr>
            <tr>
              <td>収録曲</td>
              <td>{{ doc.songs }}</td>
            </tr>
            <tr>
              <td>初出</td>
              <td>{{ doc.firstEvent }}</td>
            </tr>
            <tr>
              <td>コメント</td>
              <td>{{ doc.comment }}</td>
            </tr>
            <tr>
              <td>在庫</td>
              <td>
                {% if doc.stock == false %}
                DL版のみ
                {% else %}
                在庫あり
                {% endif %}
              </td>
            </tr>
            <tr>
              <td>XFD</td>
              <td><a href="https://nico.ms/{{ doc.xfd }}" target="_blank">{{ doc.xfd }}</a></td>
            </tr>
          </tbody>
        </table>
      </div>
    {% endif %}
  {% endfor %}
</div>
