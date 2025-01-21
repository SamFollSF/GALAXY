# Inserire Video nella documentazione

Inserire un video nella documentazione di Mkdocs è molto semplice, basterà usare un codice HTML che ho inserito qui sotto.

```
<video width="640" height="360" controls>
  <source src="../iltuovideo.mp4" type="video/mp4">
</video>
```

N.B.: Il file .mp4 deve trovarsi esattamente nello stesso percorso del file .md. Facciamo un esempio: Nella cartella X c'è il file .md, in questa stessa cartella andra inserito il file video (ti consiglio di rinominarlo in modo breve e semplice per evitare errori di battitura).