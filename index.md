---
marp: true
theme: default
style: |
  section {
    position: relative;
  }
  section::before {
    content: '';
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: url('img/vb_groupp.webp');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    opacity: 0.1;
    z-index: 0;
  }
  section > * {
    position: relative;
    z-index: 1;
  }
---
# ベリーベストの良いところ・悪いところ

**Beer Bash LT**

---

## 🎉 良いところ

---

### リモートワーク & 環境

- **ほぼフルリモート可能**
  - 柔軟な働き方ができる
- **支給されるMacがめっちゃいいやつ**
  - 開発環境に妥協なし

---

### 働きやすさ

- **業務時間が7時間30分**
  - ワークライフバランス◎
- **みんないい人**
  - 働きやすい雰囲気

---

### チャレンジできる環境

- **手を上げれば任せてくれる!**
  - 主体性を重視
- **有料サービスも業務に役立つものは積極採用**
  - Cursorなど、生産性向上ツールの導入に前向き

---

### 法務の専門性

- **弁護士の意見が聞ける**
  - 法律面での不安を解消できる貴重な環境

---

## 🌏 オフショア開発体制

---

### beetechとの連携

- **beetechというオフショアを活用中**
- **beetechを買収済み**
  - 結構自由に利用できる体制
- **皆さんの仕事も受注して対応可能!**
  - 開発リソースの柔軟な活用ができます

---

## 😅 悪いところ(改善の余地)

---

### コミュニケーション

- **Slackメインで使ってない**
  - エンジニアにとっては慣れが必要かも

---

### 文化・手続き

- **弁護士事務所ということでちょっとお硬い**
  - ベンチャー文化とは少し違う雰囲気
- **業務手続きが最初は複雑かも?**
  - Redmineで週報と日報の両方記載など

---

### 福利厚生

- **健保がITSじゃない**
  - ベンチャー系出身者には物足りないかも
  - (ITSは福利厚生が充実していることで有名)

---

### その他

- **名前と顔が永遠に一致しない**
  - リモートワークあるあるですね😅

---

## まとめ

- ✅ 働きやすい環境と自由度の高さ
- ✅ オフショア活用で開発リソース確保
- ⚠️ ベンチャーとは少し違う文化
- ⚠️ 手続き面での慣れは必要

**総じて、エンジニアとして成長できる良い環境!** 🎊

---

## ご清聴ありがとうございました! 🍺

<script>
(function() {
  const width = height = 80;
  const init = () => {
    const slides = document.querySelectorAll('section');
    if (slides.length === 0) {
      setTimeout(init, 100);
      return;
    }
    
    const totalSlides = slides.length;
    
    slides.forEach((slide, index) => {
      // 二重追加を防止
      if (slide.querySelector('.custom-progress-bar')) return;

      const currentPage = index + 1;
      const progress = (currentPage / totalSlides) * 100;
      
      // プログレスバー
      const bar = document.createElement('div');
      bar.className = 'custom-progress-bar';
      bar.style.cssText = `
        position: absolute;
        bottom: 10px;
        left: 0;
        width: 100%;
        height: 8px;
        background: linear-gradient(
          to right,
          #4CAF50 ${progress}%,
          #e0e0e0 ${progress}%
        );
        pointer-events: none;
      `;
      
      // 各スライドにドットを配置（進捗に応じた位置）
      const dot = document.createElement('img');
      dot.src = 'img/j_man_move.gif';
      dot.style.cssText = `
        position: absolute;
        bottom: 0px;
        left: calc(${progress}% - ${width/2}px);
        width: ${width}px;
        height: ${height}px;
        object-fit: contain;
        z-index: 10;
        pointer-events: none;
      `;
      
      slide.appendChild(bar);
      slide.appendChild(dot);
    });
  };

  if (document.readyState === 'loading') {
    document.addEventListener('DOMContentLoaded', init);
  } else {
    init();
  }
})();
</script>