---
title: "CDs - Le Site Web de Suika AKIYAMA"
title_for_header: "CDs"
description: "CDリスト"
---

CDリスト建設予定地

# このページは整備中です!

<!-- Auto-List Test -->
<div class="grid">
  
{% assign doclist = site.pages | sort: 'url' | reverse %}
  {% for doc in doclist %}
    {% if doc.url contains 'music/' %}
      <div class="item">
        <a href="{{ doc.url | remove: '.html' }}">
          <img class="float-left" src="{{ doc.image }}" alt="{{ doc.title }} サムネ">
        </a> 
        <h2 class="float-right" style="font-size:26px;">{{ doc.title }}</h2>
        <table class="float-right">
          <tr>
            <th>ID</th>
            <td>{{ doc.name | remove: '.md' }}</td>
          </tr>
          <tr>
            <th>作曲年</th>
            <td>{{ doc.postTime }}</td>
          </tr>
          <tr>
            <th>ニコニコ</th>
            <td><a href="https://www.nicovideo.jp/watch/{{ doc.nicoId }}" target="_blank">{{ doc.nicoId }}</a></td>
          </tr>
          <tr>
            <th>歌詞</th>
            <td>{{ doc.lyric }}</td>
          </tr>
          <tr>
            <th>収録CD</th>
            <td style="font-size:15px;">{{ doc.songIn }}</td>
          </tr>
        </table>
      </div>
    {% endif %}
  {% endfor %}

</div>
<!-- Auto-List Test End -->
