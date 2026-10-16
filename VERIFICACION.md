# ¿Qué se revisa antes de entregar un texto?

## ¿Qué se revisa de la voz?

- [ ] Las opiniones van en primera persona del singular. El plural sólo guía al lector o incluye a todos.
- [ ] No aparecen «quizás», «tal vez», «algunos creen» ni «otros interpretan» usados para esconderse.
- [ ] El autor no aparece como ejemplo, contraejemplo ni medida de nada, y no hay autobiografía inventada.
- [ ] No hay comparaciones con otros («casi nadie», «la mayoría») ni frases desde arriba.
- [ ] No se caricaturiza ni ridiculiza a nadie.
- [ ] Todos los títulos y subtítulos son preguntas, y cada capítulo cierra con una.

## ¿Qué se revisa del estilo?

- [ ] Ningún párrafo repite el anterior con otras palabras.
- [ ] No quedan adornos, imágenes decorativas ni fórmulas de relleno.
- [ ] Las frases son cortas y suenan bien en voz alta.
- [ ] El texto es lo más corto posible.

## ¿Qué se revisa de la honestidad?

- [ ] Cada afirmación de hecho está en el texto o en la fuente. Nada se afirmó de más.
- [ ] Las interpretaciones están marcadas como tales («me parece», «creo que»).
- [ ] Lo que juega en contra está nombrado.
- [ ] Las citas bíblicas coinciden letra por letra con la traducción elegida para el libro.
- [ ] Jesús, según los cuatro Evangelios, aparece como filtro en cada capítulo.

## ¿Qué búsquedas automáticas ayudan?

```bash
# Primera persona del plural que puede estar disfrazando una opinión
grep -n -E "\b(creemos|[Nn]os parece|[Dd]ecimos|preferimos|no vamos a)\b" manuscrito/*.md
# Palabras para esconderse
grep -n -E "\b([Qq]uizás?|[Tt]al vez|algunos creen|otros interpretan)\b" manuscrito/*.md
# Comparaciones y frases desde arriba
grep -n -E "casi nadie|la mayoría|muchos predicadores|para que nadie" manuscrito/*.md
# Voseo fuera de citas
grep -n -E "\b(andá|mirá|fijate|tenés|querés|sabés|vos)\b" manuscrito/*.md
```

Las coincidencias dentro de citas de personajes están permitidas.
