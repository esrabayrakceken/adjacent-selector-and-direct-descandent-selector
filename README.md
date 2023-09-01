# adjacent-selector-and-direct-descandent-selector
## Another two variants of Css selector (Css selectorun başka iki çeşidi)
### 1.Adjacent Selector:
- Ardarda gelen iki öğe kullanılarak oluşturulan selector. Soydan değil, iç içe değil, sadece ardarda gelenler.
```html
<input type="password" placeholder="password" id="password">
<button>Log In</button>
```
- Kodda __inputtan__ sonra gelen __button__ mevcut. Şimdi bu ardarda gelen 2 öğeyi kullanarak selector oluşturalım. Ve __buttona__ stil verelim.
---
```css
input+button {
              background-color:pink;
```
- __input+button:__ buttondan hemen önce gelen "input" "+" "button" şeklinde selector oluşturulur.
- __background-color:__ butonun arka plan rengini pembe yapar.
---
### 2.Direct Child(Descandent) Selector:
- Bir __div__, __li__, __nav__ içine yerleştirilmiş genel çocuklar değil de, doğrudan soydan gelen çocukları temsil eder. Ne demek istiyorum?
```html
<footer>
        <nav>
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
                <li><a href="https://www.google.com">Google</a></li>
            </ul>
        </nav>
        <a href="#licence">Content is available under these licence</a>
</footer>
```
- Yukarıdaki kodda __footer__ atasının içindeki __Home,About,Contact,Google__ genel çocuklardır. Çünkü bunların hepsi; birden çok etiket(__div__, __li__, __nav__) içine yerleştirilmiştir. En alttaki __Content is available under these licence__ ise doğrudan çocuktur. Herhangi başka bir etiket içinde değildir. Diğer bir deyişle __footerın__ bir seviye altındadır.
---
- Şimdi bu doğrudan çocuğa stil verelim.
```css
footer > a {
           color:blue;
}
```
- __footer >a:__ "footer" ">" "a" şeklinde selector oluşturulur.
- __color:blue:__ "a" etiketi içindeki __Content is available under these licence__ yazısını mavi yapar. Diğer "a" etiketlerinde herhangi bir değişiklik olmaz.
---
- Bu kullanım çok fazla tercih edilmese de kesinlikle karşılaşılabilecek bir yöntemdir.
  
 _İyi kodlamalar.._




