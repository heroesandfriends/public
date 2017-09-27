Public files for better use of Heores and friends

# how to embed an heroes and friends projet to my website?

add the reference to the widget:
`<script src='https://cdn.rawgit.com/heroesandfriends/public/master/lib/widget.min.js'></script>`

add the heroes and fiends iframe replacing `--ID-OF-MY-HF-PROJECT--` with the correct one:
```html
<div id='iframe-hf-container' style="width:100%;height:1010px;overflow:hidden">
  <iframe id='iframe-hf' src="https://www.heroesandfriends.com/embed/--ID-OF-MY-HF-PROJECT--" scrolling="yes" class="iframe-class" width='100%' height="1000px" frameborder="0"></iframe>
</div>
```

# how to setup language interface?
By default the language is setup depending on user preferences on *Heroes and Friends* plateform else by detecting browser language. However you can still set a contextual language from:
* english
* dutch
* portuguese
* french

## init a prefered language
You can force to set the *heroes and friends* iframe to be show by GET parameter using this model instead of the previous one:

```html
<div id='iframe-hf-container' style="width:100%;height:1010px;overflow:hidden">
  <iframe id='iframe-hf' src="https://www.heroesandfriends.com/embed/--ID-OF-MY-HF-PROJECT--?locale=--LANG--ID--" scrolling="yes" class="iframe-class" width='100%' height="1000px" frameborder="0"></iframe>
</div>
```

The `--LANG--ID--` could be: `en`, `nl`, `pt` or `fr`

## dynamically change the locale
On top of the previous setup, if your website is internationalized you have the possibility to update the language dynamically. By implementing this sort of `javascript` method:

````html
  <script>
    function updateLocale(){
      var locale = document.getElementById("cblang").value; // target a combo box
      widgetHF.setlocale( locale );
    }
  </script>
  
  <select id="cblang" onchange="updateLocale()">
    <option value="en"> English
    <option value="nl"> Nederland
    <option value="pt"> Portuguese
    <option value="fr"> Français
  </select>
````
