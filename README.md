# Breakout - MORAS

Projekt iz kolegija Moderni računalni sustavi.

Igra Breakout implementirana je u programskom jeziku Jack i namijenjena je izvođenju u nand2tetris VM Emulatoru.

## Opis igre

Cilj igre je platformom odbijati lopticu i uništiti sve cigle.

Igrač upravlja platformom pomoću lijeve i desne strelice. Igra završava pobjedom nakon uništavanja svih cigli ili porazom nakon gubitka svih života.

## Razine težine

Na početku igre moguće je odabrati jednu od tri težine:

- Easy: široka platforma, 10 cigli i 3 života
- Normal: srednja platforma, 20 cigli i 2 života
- Hard: uska platforma, 30 cigli i 1 život

## Upravljanje

- Lijeva strelica: pomicanje platforme ulijevo
- Desna strelica: pomicanje platforme udesno
- Tipke 1, 2 i 3: odabir razine težine

## Struktura projekta

- `Main.jack` - glavna petlja, izbornik, rezultat, životi i stanje igre
- `Game.jack` - brzina igre i učestalost iscrtavanja zaslona
- `Ball.jack` - pomicanje loptice i provjera sudara
- `Platform.jack` - pomicanje i crtanje platforme
- `Brick.jack` - prikaz i stanje pojedine cigle
- `Border.jack` - crtanje donje granice igrališta
- `.vm` datoteke - prevedene verzije Jack datoteka

## Tehnički detalji

Sudari se provjeravaju usporedbom rubova pravokutnika koji predstavljaju lopticu, platformu i cigle.

Mjesto udara loptice u platformu određuje njezin horizontalni smjer:

- lijeva trećina usmjerava lopticu ulijevo
- desna trećina usmjerava lopticu udesno
- srednja trećina mijenja postojeći horizontalni smjer

Igra koristi odvojeno ažuriranje stanja i iscrtavanje zaslona radi učinkovitijeg izvođenja.

## Autor

Ime i prezime: Lovro Ćosić 
Kolegij: Moderni računalni sustavi
