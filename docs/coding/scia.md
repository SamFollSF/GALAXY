---
tags:
    - Coding
---

## Come mettere la scia al cursore

Inserire una scia al cursore è molto semplice, ora ti mostrerò come fare.

Comincia creando nella cartella "assets" (docs>assets) due file: Uno con il nome di "cursor.js" e l'altro "style.css".

Una volta fatto ciò dovrai importare nella stessa cartella (assets) un file .png che vogliamo sia la nostra scia. (Ti consiglio un nome breve e facile da scrivere)

Fatto ciò abbiamo bisogno dei contenuti per i 2 file, li troverai qui di seguito.

### Contenuto file "cursor.js"

```
 document.addEventListener('DOMContentLoaded', function() {
    var cursorTrail = document.createElement('div');
    cursorTrail.classList.add('cursor-trail');
    document.body.appendChild(cursorTrail);

    document.addEventListener('mousemove', function(event) {
        cursorTrail.style.left = event.pageX + 'px';
        cursorTrail.style.top = event.pageY + 'px';
    });
 });
 /{
    let trailElement = document.createElement('div');
    trailElement.classList.add('cursor-trail');
    document.body.appendChild(trailElement);
    
    trailElement.style.left = `${event.pageX}px`;
    trailElement.style.top = `${event.pageY}px`;
    
    if (trail.length > trailLength) {
        let firstElement = trail.shift();
        firstElement.remove();
    }
 }
```

### Contenuto file "style.css"

```
.cursor-trail {
    position: absolute;
    pointer-events: none;
    width: 30px;
    height: 30px;
    background-image: url('scia.png');
    background-size: contain;
    background-repeat: no-repeat;
    transform: translate(-50%, -50%);
    z-index: 9999;
    opacity: 0.7;
    pointer-events: none;
    transition: transform 0.1s ease-out
  }
```
NOTA: Al rigo 6 in questo codice il mio file si chiama "scia.png", in questo spazio dovrai inserire il nome del tuo file ('esempio.png'). Un consiglio: non inserire il percorso del file, mkdown ti dirà che non troverà il png, segui esattamente questa ortografia.

### Creare gli extra nel file mkdocs.yml

Dopodiché dovrai inserire in fondo al tuo file "mkdocs.yml" questo codice:

```
extra_javascript:
  - assets/cursor.js

extra_css:
  - assets/style.css
```

## Conclusioni

Ricorda di salvare tutte le modifiche usando <kbd>Ctrl</kbd> + <kbd>S</kbd>, di prestare molta attenzione all'ortografia e dove inserisci i tuoi file. Detto ciò dovresti vedere la tua scia sul tuo sito.

You're Welcome.