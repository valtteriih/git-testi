19.4.2022 11.28 aloin työstämään tämän viikon tehtävää. Kurssisivu https://terokarvinen.com/2021/configuration-management-systems-2022-spring/

H3 Versionhallinta

Z) Lue ja tiivistä arrtikkeli https://commonmark.org/help/
   Tämä artikkeli kertoo yleisiä komentoja ja neuvoja siihen että miten markdownia käytetään

A) Tee tehätävän raportti markdownina

B) Tein aluksi tiedostot laksy1.md ja laksy2.md, annoin commit tekstiksi Add top level menu to Foobar synchronizer jonka jälkeen tein niille muutoksia, 
muutin tiedostojen tekstiä ja annoin niille yhden saman commit tekstin, add changes to laksy 1 and laksy2 files,
sen jälkeen tein niihin vielä yhdet muutokset (taas vain tekstiin) ja annoin vielä yhteisen commit tekstin Add top level menu to Foobar synchronizer
nano laksy1.md
nano laksy2.md
git add .
git commit
git pull
git push

C) Git log komento näyttää muutokset ja commit tekstit niihin teidstoihin mitä on luotu tai muokattu
   Git diff komento näyttää muutokset committien, "työpuun" ja indeksin välillä
   Git blame komento näyttää kuka on viimeksi muokannut tiedostoa ja mitäkin riviä
git log
git diff
git blame

D) Kokeilin tätä tehtävää niin että muutin laksy1.md teidostoa siten että poistin sieltä kaiken tekstin ja laitoin sinne tekstin postetaan täältä teksti ja tallensin tiedoston.
Sitten vain ajoin komennon git reset --hard ja avasin tiedoston, tiedoston teksti oli entisellään niin kuin en olisi sitä ikinä muuttanutkaan.
nano lasky1.md
git reset --hard

E) tein todella yksinkertaisen file.managed tilan. Tein kansioon /srv/salt tiedsoton hello.sls jonne kirjoitin seuraavan pätkän. 
/tmp/hellovaltteri.txt:
  file.managed:
    - source: salt://hellovaltteri.txt
sitten tein samaan kansioon hellovaltteri.txt tiedoston jonna laitoin vain tekstin hello valtteri.
Sitten ajoin sen komennola sudo salt ’*’ state.apply hello.
Käytin apuna kyseistä ohjetta https://terokarvinen.com/2018/salt-states-i-want-my-computers-like-this/ 
sudo nano hello.sls
sudo nano hellovaltteri.txt
sudo salt ’*’ state.apply hello

lopetin kirjoituksen klo 12.45

pohjana tero karvisen kurssi 

https://terokarvinen.com/2021/configuration-management-systems-2022-spring/
