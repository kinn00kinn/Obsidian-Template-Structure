---
tags:
  - "#daily"
---
# 🌟 Daily Template - {{date:YYYY-MM-DD}} 



---

## 📺 News & Updates

<%* 
async function getYahooNews() {
  const rssUrl = "https://news.yahoo.co.jp/rss/topics/top-picks.xml";

  try {
    //Templaterの関数を使ってrequestを送る
    const response = await tp.obsidian.requestUrl(rssUrl);
    if (response.status != 200) {
      return "ニュースの取得に失敗しました。";
    }

    const xml = await response.text;

    // ニュースアイテムを抽出
    const items = xml.match(/<item>([\s\S]*?)<\/item>/g);
    if (items && items.length > 0) {
      let newsList = "### 今日のYahooニュース\n\n";
      for (let i = 0; i < Math.min(items.length, 10); i++) {
        const titleMatch = items[i].match(/<title>(.*?)<\/title>/);
        const linkMatch = items[i].match(/<link>(.*?)<\/link>/);

        const title = titleMatch ? titleMatch[1] : "タイトル不明";
        const link = linkMatch ? linkMatch[1] : "#";

        newsList += `- [${title}](${link})\n`;
      }
      return newsList;
    } else {
      return "ニュースが見つかりませんでした。";
    }
  } catch (error) {
    return `エラーが発生しました: ${error.message}`;
  }
}
const news = await getYahooNews();
tR += news;
%>


---

## 🔥 Today’s Mood & Reflections
- 


---



## 📖 Daily Diary
**今日感じたこと、アイデアや気づき、メモしたいこと**  
- 

---



## 🎥 Watch Later
（気になる動画，映画，記事）
- 
- 

---

tags: #{{date:YYYY-MM}} #daily