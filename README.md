# submona web font

![サブモナーフォント](submona.png)

The original [monafont](http://monafont.sourceforge.net/) is an extensive typeset: the file size of its TTF is about 3 MB, so even after compression it's still probably too big to be used as a web font. The *submona* web font project attempts to create a lightweight subset (52 KB) of *monafont* that can render common Shift_JIS text art in an acceptable manner, by removing the embedded bitmap strikes (a.k.a. pixel fonts) and many glyphs from some Unicode ranges. The results might not be always perfect but should be good enough for the appreciation of casual users :-)

## Usage

Add a new `@font-face` at-rule for *submona* into your CSS, and then append the new *submona* font-family to the class you already use for Shift_JIS art. It will look something like this:

```css
@font-face {
  font-family: 'submona';
  src: url('submona.woff') format('woff');
}

.sjis {
  font-family: IPAMonaPGothic, 'IPA モナー Pゴシック', Monapo, Mona, 'MS Pgothic', 'MS Pゴシック', submona;
}
```
