# Immagini Ridimensionate

Ho da poco scoperto come poter ridimensionare le immagini su Mkdocs senza utilizzare codici HTML. Vediamo insieme come fare.

Il codice è un aggiornamento dell'ormai celebre ```![nome](../percorso)"```.

```
![Testo alternativo](percorso/dell/immagine.jpg){: style="display: block; margin-left: auto; margin-right: auto; width:300px;" }
```

La prima parte rimane invariata, mentre la seconda permette l'allineamnto al centro. L'unica cosa che consiglio di modificare a proprio piacimento è il valore "width:300px" con il numero di pixel (e quindi dimensione) della foto.