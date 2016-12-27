---
layout: default
title: Kontakt
---

<div id="contact">
  <h1 class="pageTitle">Kontakt</h1>
  <div class="contactContent">
    <p class="intro">Masz jakieś pytania? Pisz śmiało!</p>
    <p>Jeśli tylko będę w stanie pomóc, z chęcią wtopię zęby w temat.</p>
  </div>
  <form action="http://formspree.io/your@mail.com" method="POST">
    <label for="name">Imię i nazwisko</label>
    <input type="text" id="name" name="name" class="full-width"><br>
    <label for="email">Email</label>
    <input type="email" id="email" name="_replyto" class="full-width"><br>
    <label for="message">Wiadomość</label>
    <textarea name="message" id="message" cols="30" rows="10" class="full-width"></textarea><br>
    <input type="submit" value="Niechaj leci!" class="button">
  </form>
</div>
