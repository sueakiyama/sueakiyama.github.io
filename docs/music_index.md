---
title: "Musique - Le Site Web de Suika AKIYAMA"
title_for_header: "Musique"
description: "<a href='https://sueakiyama.github.io/' style='color:#ffffff'><u>Le Site Web de Suika Akiyama</u></a>"
---

<!-- Auto-List Test -->
<div class="grid">
  
{% assign doclist = site.pages | sort: 'url' | reverse %}
  {% for doc in doclist %}
    {% if doc.url contains 'music/' %}
      <div class="item">
        <a href="{{ doc.url }}">
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
            <td><a href="https://www.nicovideo.jp/watch/{{ doc.nicoId }}">{{ doc.nicoId }}</a></td>
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

<div class="grid">
  <div class="item">
    <a href="music/aki65.html">
      <img class="float-left" src="https://sueakiyama.github.io/music/images/aki65.png" alt="アンドロイドは夢を見ない サムネ">
    </a> 
    <h2 class="float-right" style="font-size:26px;">アンドロイドは夢を見ない</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki65</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2023年10月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://www.nicovideo.jp/watch/sm43048884">sm43048884</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>夜が来て、目を閉じても……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td style="font-size:15px;">アンドロイドは夢を見ない</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki54.html">
      <img class="float-left" src="https://sueakiyama.github.io/illustrations/images/20230216_1.png" alt="春休み2週間目サムネ">
    </a> 
    <h2 class="float-right">春休み2週間目</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki54</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2023年2月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://www.nicovideo.jp/watch/sm41805954">sm41805954</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>春休み2週間目 やりたいこと……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>100年寝たい</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki51.html">
      <img class="float-left" src="https://sueakiyama.github.io/images/20221227.png" alt="逆たまごかけごはんジャケット">
    </a> 
    <h2 class="float-right">セカンドハンド・<br>ラブストーリー</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki51</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2022年12月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td>なし</td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>「すき」とか「愛してる」とか……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki47.html">
      <img class="float-left" src="music/images/aki47.jpg" alt="逆たまごかけごはんサムネイル">
    </a> 
    <h2 class="float-right">逆たまごかけごはん</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki47</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2022年10月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://nico.ms/sm41194270">sm41194270</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>割れたたまごが元には戻らないように……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki44.html">
      <img class="float-left" src="music/images/aki44.jpeg" alt="蝉みたいに不器用でサムネイル">
    </a> 
    <h2 class="float-right">蝉みたいに不器用で。</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki44</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2022年9月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://nico.ms/sm41110114">sm41110114</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>日に焼けたアスファルトのにおいと……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki36.html">
      <img class="float-left" src="music/images/aki36.jpg" alt="忘却概論サムネイル">
    </a> 
    <h2 class="float-right">忘却概論</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki36</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2021年7月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://nico.ms/sm39170091">sm39170091</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>ひとの名前は覚えない……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki32.html">
      <img class="float-left" src="music/images/aki32.jpg" alt="サイダーブルーサムネイル">
    </a> 
    <h2 class="float-right">サイダーブルー</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki32</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2021年4月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://nico.ms/sm39170091">sm39170091</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>詩を書くのは得意じゃなくて……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki27.html">
      <img class="float-left" src="music/images/aki27.jpg" alt="エリアメール変奏曲サムネイル">
    </a> 
    <h2 class="float-right">エリアメール変奏曲</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki27</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2020年10月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://nico.ms/sm38712935">sm38712935</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>ああ、聞こえない、しどけない……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
  <div class="item">
    <a href="music/aki26.html">
      <img class="float-left" src="music/images/aki26.jpg" alt="日常系ヒゲンジツサムネイル">
    </a> 
    <h2 class="float-right">日常系ヒゲンジツ</h2>
    <table class="float-right">
      <tr>
        <th>ID</th>
        <td>aki26</td>
      </tr>
      <tr>
        <th>作曲年</th>
        <td>2020年8月</td>
      </tr>
      <tr>
        <th>ニコニコ</th>
        <td><a href="https://nico.ms/sm37384763">sm37384763</a></td>
      </tr>
      <tr>
        <th>歌詞</th>
        <td>将来の夢も展望も……</td>
      </tr>
      <tr>
        <th>収録CD</th>
        <td>逆たまごかけごはん</td>
      </tr>
    </table>
  </div>
</div>
