Public files for better use of Heores and friends

# how to embed an heroes and friends projet to my website?

add the reference to the widget:
`<script src='https://raw.githubusercontent.com/heroesandfriends/public/master/lib/widget.min.js'></script>`

add the heroes and fiends iframe replacing `--ID-OF-MY-HF-PROJECT--` with the correct one:
```html
<div id='iframe-hf-container' style="width:100%;height:1010px;overflow:hidden">
  <iframe id='iframe-hf' src="https://www.heroesandfriends.com/embed/--ID-OF-MY-HF-PROJECT--" scrolling="yes" class="iframe-class" width='100%' height="1000px" frameborder="0"></iframe>
</div>
```
