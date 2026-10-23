# ¿Qué se revisa antes de entregar un texto?

## ¿Qué se revisa de la voz?

- [ ] Las opiniones van en primera persona del singular. El plural sólo guía al lector o incluye a todos.
- [ ] No aparecen «quizás», «tal vez», «algunos creen» ni «otros interpretan» usados para esconderse.
- [ ] El autor no aparece como ejemplo, contraejemplo ni medida de nada, y no hay autobiografía inventada.
- [ ] No hay comparaciones con otros («casi nadie», «la mayoría») ni frases desde arriba.
- [ ] No se caricaturiza ni ridiculiza a nadie.
- [ ] Todos los títulos y subtítulos son preguntas. Cada capítulo cierra con una pregunta o con una línea final que deja abierta la pregunta («Ahora prepara otra», «El manto ya cambió de manos»). No se agrega una pregunta floja sólo para cumplir.

## ¿Qué se revisa del estilo?

- [ ] Ningún párrafo repite el anterior con otras palabras.
- [ ] No quedan adornos, imágenes decorativas ni fórmulas de relleno.
- [ ] Las frases son cortas y suenan bien en voz alta.
- [ ] El texto es lo más corto posible.

## ¿Qué se revisa de la honestidad?

- [ ] Cada afirmación de hecho está en el texto o en la fuente. Nada se afirmó de más.
- [ ] Las interpretaciones están marcadas como tales («me parece», «creo que»).
- [ ] Lo que juega en contra está nombrado (en un libro; en un post no hay sección de objeciones, ver `TIPOS-DE-LIBRO.md`).
- [ ] En un post: está lleno de preguntas, entra directo al planteo y cierra con una pregunta para el lector, sin moraleja.
- [ ] Las citas bíblicas coinciden letra por letra con la traducción elegida para el libro.
- [ ] Jesús gobierna la interpretación de cada capítulo y aparece explícitamente cuando la comparación aporta algo; un arco de varios capítulos puede reservar la escena de los Evangelios para el lugar donde tiene más fuerza. Nunca se agrega una escena de Jesús sólo para cumplir una cuota.

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
