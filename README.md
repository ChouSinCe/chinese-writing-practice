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

## Test mode

Press **Start test** to take a test on the sentences in the box. The sentence list is hidden, so only the pinyin shows. The child writes (or types) every character, then presses **Check my test** once at the bottom. The page marks every character and shows the score as a percentage, with the characters to practise. **Practise mistakes again** starts a new test with only the sentences that had mistakes. **Exit test** goes back to practice.

## Checking answers

- **Typing mode** is checked automatically, character by character.
- **Writing mode**: the child writes freely in the boxes, then presses **Check my writing**. Each character is compared stroke by stroke with the real character. Stroke order and stroke direction do not matter; a missing stroke, an extra stroke, or a stroke in the wrong place is marked wrong. Tap a box to change its mark if you disagree.

Stroke shapes come from the free [hanzi-writer-data](https://github.com/chanind/hanzi-writer-data) set. The check is forgiving about size and proportions, so very similar characters with the same number of strokes (for example 未/末, 人/入, 田/由) may not be told apart. Tap the box to mark those yourself.

## Notes

- Pinyin comes from [pinyin-pro](https://github.com/zh-lx/pinyin-pro) and follows context for most characters with more than one reading (长大 zhǎng, 银行 háng). Check unusual words and names.
- The sentence list and answer mode are saved in the browser's local storage, so they are still there next time on the same device.
