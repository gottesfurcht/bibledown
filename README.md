# Bibledown

**Bibledown** is a new Bible file format. All of the existing Bible formats require special Bible programs to render the text, i.e. to make it readable.

This new format is called **Bibledown** and is based on the popular [Markdown](https://en.wikipedia.org/wiki/Markdown) markup language. The text can be rendered with normal Markdown tools (like Github is using here for example).

Additional information like verse numbers, chapter, book info etc. is added with html markup between the lines, which is ignored when the Markdown is rendered. Special programs **can** use this information for additional features, but special programs are **not neeeded**.

## Format

For a live example, please see the project [Zürcher Bibel](https://github.com/gottesfurcht/zuercher-bibel).

The formatting (like headings, paragraphs, bold text etc.) is achieved by Markdown markup. Here we have a short example:

```md
<collection>

## <title>Das neu Testament</title>

<book id="John">

### <title>Euangelion Sankt Johannes</title>

<chapter id="1">

#### <title>Das erst Capitel</title>

<section id="a">
<verse id="1">Im anfang war das wort, und das wort war bei Gott, und Gott war das wort.</verse>
<verse id="2">Das selbig war im anfang bei Gott.</verse>
<verse id="3">Alle ding sind durch das selbig gemachet, und ohn das selbig ist nichts gemachet was gemachet 
</section>
</chapter>
</book>
</collection>
```

Html tags are used to designate a `book` or a `collection` (of books). The `id` attribute indicates a `chapter` number, a `section` or a `verse` number.
