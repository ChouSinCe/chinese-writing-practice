# 拼音听写 Pinyin Dictation

A simple web page for practising Chinese characters (汉字) at home.

1. Type or paste Chinese sentences, one per line.
2. The page shows the pinyin above empty 田字格 boxes.
3. The child writes each character in the boxes (finger or stylus), or types them with a Chinese keyboard.
4. Check the answers. The score shows which characters were wrong, and **Practise mistakes again** builds a new round from those sentences.

## Files

- `index.html` – the whole app in one file. No build step, no server needed.

## Run it

- **On your computer:** double-click `index.html` to open it in a browser.
- **On GitHub Pages:** put `index.html` in the repo, then go to **Settings → Pages**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save. The page will be live at `https://<your-username>.github.io/<repo-name>/` after a minute or two.

An internet connection is needed the first time, because the pinyin library and fonts load from a CDN.

## Checking answers

- **Typing mode** is checked automatically, character by character.
- **Writing mode** shows the correct characters faintly behind the child's writing. Tap any box that is wrong to mark it.

Automatic handwriting checking by Claude only works when the page is opened as a Claude artifact. On GitHub Pages or a local file, writing mode uses the tap-to-mark check instead.

## Notes

- Pinyin comes from [pinyin-pro](https://github.com/zh-lx/pinyin-pro) and follows context for most characters with more than one reading (长大 zhǎng, 银行 háng). Check unusual words and names.
- The sentence list and answer mode are saved in the browser's local storage, so they are still there next time on the same device.
