# Linux 101

* [Korte Linux Command Line Interface (CLI) tutorial van Digital Ocean](https://www.digitalocean.com/community/tutorials/an-introduction-to-linux-basics): essentiele basis om te navigeren in de CLI. *Noot:* In plaats van 'nano' kan je ook een betere editor gebruiken (vim en emacs zijn meer advanced CLI editors, gedit is een grafisch alternatief met syntax highlighting).

* [Uitgebreidere tutorial](http://linuxcommand.org/): optioneel (veel meer in-depth)

* [Commando Cheatsheet](https://github.com/ComputerGraphicsResearchGroup/peno3/blob/gh-pages/tools/LinuxCheatsheet.md)

* Enkele andere commando's:
  * `CTRL-C`: Cancel, i.e. abort abort abort. Te gebruiken als je het programma in de terminal wil afbreken.
  * `CTRL-D`: End-Of-File/End-Of-Transmission, i.e. geeft aan dat je klaar bent met wat je bezig was en wil stoppen. Dit kan je gebruiken om terminals te sluiten en werkt ook om de (i)python interpreter af te sluiten.
  * `CTRL-C` en `CTRL-V` werkt doorgaans zoals verwacht, maar er is nog een handig alternatief om te copy-pasten. Eender welke tekst die je met de muis geselecteerd hebt, zit automatisch in een speciale selection buffer dewelke je kan 'plakken' op de huidige cursorpositie door op de middelste muisknop te klikken (i.e. copy and paste zonder het keybeard te gebruiken). In plaats van de middelste muisknop te gebruiken, kan je dit evenzeer 'plakken' met de combinatie `SHIFT+INSERT` op het keyboard.
  * `;` kan commando's 'chainen', e.g. `echo hallo; echo wereld`. Belangrijk: ook als het eerste commando faalt, zal het tweede commando worden uitgevoerd.
  * `&&` kan commando's 'chainen' waarbij wordt gestopt indien het eerste commando faalt. e.g. `false && echo juist` (zoek eens `man false` en `man true`, het doet inderdaad wat je zou verwachten). Merk op: de `&&` is dus exact hetzelfde als een 'lazy and' vanuit je favoriete programmeertaal.
  * Om python op te roepen: `python path\_naar\_python\_file.py`
    e.g.: `python Documenten/awesomeMonteCarloSampler.py`
    of: `cd Documenten && python awesomeMonteCarloSampler.py`
  * In een (deftige) command line interface (zoals de shell die je standaard krijgt als je een terminal opent, alsook binnen de python interperter, etc) heb je een aantal handige keyboard shortcuts die je constant zal gebruiken. Zo kan je met het pijltje omhoog terug het vorige commando krijgen (twee keer drukken voor het commando daarvoor, pijltje omlaag om terug tegaan, etc.). Met `CTRL-W` kan je het woord voor de cursor verwijderen, etc. Voor de geinteresseerden: deze functionaliteit wordt doorgaans verzord door de "readline" library. Een volledige documentatie van alle shortcuts vind je bijvoorbeeld [hier](https://cnswww.cns.cwru.edu/php/chet/readline/rltop.html#Documentation).
