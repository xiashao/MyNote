title:: TextView Line Height

- [[Mar 14th, 2022]]
- ## Text View Structure #card
  card-last-interval:: 4
  card-repeats:: 1
  card-ease-factor:: 2.6
  card-next-schedule:: 2022-03-21T05:07:29.252Z
  card-last-reviewed:: 2022-03-17T05:07:29.253Z
  card-last-score:: 5
	- ![image.png](../assets/image_1647249506338_0.png){:height 292, :width 612}
- ## Defination
- Leading, is the space between adjacent lines of type, in most cases, the value is 0.
- ## OneLine TextView Case
	- Text Height = Ascent - Descent
	- Line height = Top - Bottom = Text Height + font padding
- ## TwoLine TextView Case
	- Line Height = Text Height * 2 + font padding + leading
- ## Two TextView
	- Line Height = Text Height *2 + 2 * font padding
	- Two TextView with "includeFontPadding = false"
		- Line Height = Text Height *2
	-
- Reference:
	- [神奇的TextView](https://codeantenna.com/a/qTS5cygDkQ)
	- [Android 字体全攻略](https://www.jianshu.com/p/35328f7ac54a)
	-
	-