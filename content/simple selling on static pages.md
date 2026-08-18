---
publish: true
created: 2026-08-18T15:11:55.254Z
modified: 2026-08-18T21:59:00.370Z
---

# der einfachste shop

einen onlineshop mit statischen seiten zu betreiben erscheint unsinnig, jedoch bietet [Lemon Squeezy](https://www.lemonsqueezy.com/) (und bald stripe) einen simplen checkout link an.

er verkauft als [merchant of record](https://stripe.com/de/resources/more/merchant-of-record#was-ist-ein-eingetragener-handler) dir die freiheit von compliance und deinen kunden deine ware.

produktbeschreibung, bilder, faq und alles andere können ganz normale statische seiten bleiben. erst in dem moment, in dem jemand wirklich kaufen möchte, verlässt man die eigene seite und übergibt den komplizierten teil.

## der ganze shop

so simpel wie ein weblink

```
  [lemonsqueezy-button](https://DEIN-STORE.lemonsqueezy.com/checkout/buy/DEINE-ID)
```

[lemonsqueezy-button](https://DEIN-STORE.lemonsqueezy.com/checkout/buy/DEINE-ID)

damit wird aus praktisch jeder statischen seite eine produktseite:

```md
# mein produkt

eine kurze beschreibung, warum dieses ding existiert.

## 19 €

[jetzt kaufen](https://DEIN-STORE.lemonsqueezy.com/checkout/buy/DEINE-ID)
```

kein warenkorb keine datenverarbeitung, kein checkout-code, keine zahlungslogik in der eigenen seite.

## etwas hübscher

oder natürlich mit ein wenig css auch hübscher

```html
<a
  class="buy-button"
  href="https://DEIN-STORE.lemonsqueezy.com/checkout/buy/DEINE-ID"
>
  jetzt kaufen
</a>
```

```css
.buy-button {
  display: inline-block;
  padding: 0.75rem 1rem;
  border: 1px solid currentColor;
  border-radius: 0.5rem;
  text-decoration: none;
  font-weight: 600;
}

.buy-button:hover {
  transform: translateY(-1px);
}
```

und plötzlich sieht der weblink schon verdächtig nach shop aus.

## warum statisch?

für wenige produkte ist ein klassisches shopsystem schnell mehr aufwand als man für diese eine idee am freitagabend aufbringen möchte.

bei einer statischen seite bleibt das modell angenehm klein:

```text
produktseite

checkout-link

zahlung

produkt
```

die eigene website muss dabei nicht wissen, wer was kauft. sie muss nicht einmal wissen, was ein checkout ist. sie kennt lediglich eine url.

## das schöne daran

seiten lassen sich schnell kopieren, anpassen oder löschen.

```text
/products/ebook
/products/template
/products/course
```

jede davon kann einen eigenen checkout-link besitzen.

damit lässt sich ein kleiner shop genauso behandeln wie der rest einer statischen website: als textdateien im repository.
