# Introduktion till webbutveckling

## Mjukvara
### Visual Studio Code
* Installerad sen tidigare.

### Uppdatera Windows
- Ni vill ha Windows 10, Version 2004, Build 19041 eller högre.
- Skriv in `winver` i PowerShell för att kolla version.
- Gå in i Windows Update och ladda ned senaste.

### Node.js
- Ladda ner och installera [Node](https://nodejs.org/en/) (LTS).
- Ni kan testa att ni lyckats installera Node korrekt genom att köra en .js-fil i vs code (som när ni kör en pythonfil)
```javascript
var test = "Hello world!"
console.log(test)
```

### Windows Terminal
- Ladda ned [Windows Terminal](https://www.microsoft.com/sv-se/p/windows-terminal/9n0dx20hk701).
- Öppna settings i terminlan och välja sedan "Open JSON file".
- Byt colorScheme med följande snippet:
```json
    "profiles": {
        "defaults": {
            // Put settings here that you want to apply to all profiles.
            "colorScheme": "One Half Dark"
        },
```
- Du kan [ladda ned ett eget theme härifrån](https://atomcorp.github.io/themes/). Välj theme, copy to clipboard och lägg till i följande lista:
```json
    "schemes": [],
```

### GitHub
* Skapa ett [GitHub](https://github.com/) konto med din @edu.umea.se mail.
* Skapa ett privat repo som du kallar **webdevpriv**.
* Skapa ett publikt repo som du kallar **webdevpub**.
* Gör en ny fil som du kallar index.html i **webdevpub**  som har följande kod (klicka på **creating a new file**)

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Title</title>
  </head>
  <body>
    <div>
        <p>Hello World!</p>
    </div>
  </body>
</html>
```

* Slå på GitHub Pages för webdevpub. Låt den ha branch main som source i `/(root)` och välj inget theme.

### Git
* Du kommer bli tvungen att ställa in så att din dator kan läsa och skriva till GitHub. För att göra detta behöver du generera en ssh-nyckel i PowerShell.

```bash
ssh-keygen -t rsa -b 4096 -C "uname@edu.umea.se"
cat ~/.ssh/id_rsa.pub
```

Den publika nyckeln kommer se ut på följande format:

```bash
ssh-rsa AAAAB3NzaC1yc2EAAAABIwAAAQEAklOUpkDHrfHY17SbrmTIpNLTGK9Tjom/BWDSU
GPl+nafzlHDTYW7hdI4yZ5ew18JH4JW9jbhUFrviQzM7xlELEVf4h9lFX5QVkbPppSwg0cda3
Pbv7kOdJ/MTyBlWXFCR+HAo3FXRitBqxiX1nKhXpHAZsMciLq8V6RjsNAQwdsdMFvSlVK/7XA
t3FaoJoAsncM1Q9x5+3V0Ww68/eIFmb1zuUFljQJKprrX88XypNDvjYNby6vw/Pb0rwert/En
mZ+AW4OZPnTPI89ZPmVMLuayrD2cE86Z/il8b+gw3r3+1nKatmIkjn2so1d01QraTlMqVSsbx
NrRFi9wrf+M7Q== schacon@mylaptop.local
```

Nyckeln läggs till under settings > SSH and GPG keys på din användare på GitHub.

Ladda sedan ned Git till din dator. [Ladda ned här!](https://git-scm.com/downloads)

* Du behöver kunna följande kommandon:
  * **git config --global user.name "FIRST_NAME LAST_NAME"** för att kunna pusha.
  * **git config --global user.email "MY_NAME@example.com"** för att kuna pusha.
  * **git clone https://github.com/user-name/repository-name.git** för att hämta ned ett repo för första gången.
  * **git add .** för att lägga till alla filer i nuvarande folder och alla filer i dess undermappar.
  * **git status** för att kolla status på alla filer i ditt lokala git repo.
  * **git commit -am "Meddelande som beskriver vad du gjort"** för att spara förändringar till dina filer lokalt.
  * **git push origin master** för att pusha förändringar till ditt repo för första gången.
  * **git push** för att pusha lokalt sparade förändringar till ditt repo.
* Sätt ett bokmärke på [Git Cheat Sheet](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf).

---

* Kopiera följande till en fil som måste heta `.gitignore` och spara den i både ditt publika och privata repo:

```
# Created by https://www.toptal.com/developers/gitignore/api/visualstudiocode
# Edit at https://www.toptal.com/developers/gitignore?templates=visualstudiocode

### VisualStudioCode ###
.vscode/*
!.vscode/settings.json
!.vscode/tasks.json
!.vscode/launch.json
!.vscode/extensions.json
*.code-workspace

### VisualStudioCode Patch ###
# Ignore all local history of files
.history

# End of https://www.toptal.com/developers/gitignore/api/visualstudiocode
```
* Lägg till, committa och pusha upp dessa filer till ditt GitHub med kommandona som beskrivits ovan.

### Övrigt

Nu är du klar! Din nästa uppgift är [teoriuppgift 1](/theory_assignment_1.md).  
