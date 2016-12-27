---
layout: post
title:  "Pierwszy (po)świąteczny post za płot"
date:   2016-12-27
image: posty-za-ploty.jpeg
tags: ogolne
---

<p class="intro"><span class="dropcap">P</span>onoć początki są najtrudniejsze. Ten początek będzie jednak najprostrzy ze wszystkich. Zwyczajnie przetestuję jekyll'a.</p>

## Codesnippet?
Sprawdźmy, jak prezentuje się code snippet:
<figure>
  {% highlight python %}
  def welcome(name):
    print('Witaj na moim blogu! %s, czuj się jak u siebie.' % (name))

  ~> welcome('Gościu')
  (c)~> Witaj na moim blogu! Gościu, czuj się jak u siebie.{% endhighlight %}
  <figcaption>Code #1: Prosty, szybki, witający program.</figcaption>
</figure>

Nie jest źle. Pewnie z czasem będziemy bawić się kolorami tak by całość wyglądała zgrabniej i powabniej.

### Artykuły
Skoro jesteśmy już przy wyświetlaniu kodu, wprowadźmy na szybko link do artykułów.
W pliku: **\_config.yml** wyszukujemy sekcji **navigation:**
<figure>
  {% highlight YAML %}
  navigation:
   - title: Główna
     url: /index.html
   - title: Artykuły     # dopisujemy nazwę linka
     url: /articles      # dopisujemy ścieżkę
   - title: O mnie
     url: /about
   - title: Kontakt
     url: /contact {% endhighlight %}
     <figcaption>Code #2: Dopisanie odnośnika do artykułów.</figcaption>
</figure>

Zapisujemy zmiany w pliku **\_config.yml**, restartujemy serwer jekyll'a ażeby nasz kolega wczytał na nowo plik konfiguracyjny:
{% highlight bash %}
~> ^C               ** Zamykam poprzednią sesję kombinacją: CTRL-c **
~> jekyll s         ** Uruchamiamy na nowo serwer jekyll'a **

Configuration file: /Volumes/Work/gregdoros.github.io/\_config.yml
Configuration file: /Volumes/Work/gregdoros.github.io/\_config.yml
            Source: /Volumes/Work/gregdoros.github.io
       Destination: /Volumes/Work/gregdoros.github.io/\_site
 Incremental build: disabled. Enable with --incremental
      Generating...
                    done in 0.227 seconds.
 Auto-regeneration: enabled for '/Volumes/Work/gregdoros.github.io'
Configuration file: /Volumes/Work/gregdoros.github.io/\_config.yml
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.{% endhighlight %}
Cieszymy się z nowo powstałego odnośnika. No i przy okazji nauczyłem się korzystać z Codesnippet.

## Markdown?
Przyznam się bez bicia, Markdown to dla mnie absolutna nowość. Pisanie w nim z pewnością przysporzy kilka zagwozdek. No ale kto przy Markdown'ie nie czuje się jak hacker? Ja zdecydowanie. Czuję się. Jak hacker.

[jekyll-gh]: https://github.com/mojombo/jekyll
[jekyll]:    http://jekyllrb.com
