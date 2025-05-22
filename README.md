# Some tools

### text-splitter
Splits text. Accepts txt and epub file formats. I use it to feed text into chatgpt for translation.

https://tiklii.github.io/tools/split.html

### txt to epub
Many chinese wn websites have a download feature that provides chapters in a big-ass txt file. Chapters are partitioned by two newlines. Made this since I was following https://www.deqixs.com/xiaoshuo/331/ daily.

https://tiklii.github.io/tools/txt2epub.html

### General purpose chapter downloader (userscript)

https://gist.github.com/tiklii/715c82d5dd06d701b4773c9eea65d4c5

Kinda works. Bare bones. I made this for websites that don't work with WebToEpub. Features/Peculiarities:
- Bring your own chapter urls
- fill chapter content selectors
- Caches stuff. So you can scrape until you hit rate limits --> change vpn --> solve captcha --> and so on.
- Still has some epub styling problems. Fix manually in Calibre.
