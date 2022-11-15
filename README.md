# Durham 

```
<tr>
<td class='leftCell'><p class='dialog'><span class='kvp' data-key='prayers_gr_GR_cog|enarxis02'>Εὐλογημένη ἡ Βασιλεία τοῦ Πατρὸς καὶ τοῦ Υἱοῦ καὶ τοῦ Ἁγίου Πνεύματος, νῦν καὶ ἀεί, καὶ εἰς τοὺς αἰῶνας τῶν αἰώνων.</span>
</p></td>
<td class='rightCell'><p class='dialog'><span class='kvp' data-key='prayers_en_US_goa|enarxis02'>Blessed is the Kingdom of the Father and of the Son and of the Holy Spirit, now and forever and to the ages of ages.</span> </p></td>
</tr>
```

Deleting a table row:

- It can simply be deleted. 

Adding a table row:

1. The text visible to the user is always wrapped in a span whose class is kvp (key-value-pair):

```
<span class='kvp' data-key='prayers_en_US_goa|enarxis02'>
    Blessed is the Kingdom of the Father and of the Son and of the Holy Spirit, now and forever and to the ages of ages.
</span>
```

2. The kvp span is always wrapped in a paragraph ```<p></p>```.  The class name must match an entry in the CSS.  When deciding which class to use, inspect existing text to see what was used based on the type of text (actor, dialog, hymn, verse, etc.).

3. The enclosing paragraph is always wrapped in a table cell tag: ```<td></td>```.   

4. In order for OLW to create a meta-template from the HTML, there must be a Greek ```<td class='leftCell'>``` and a second ```<td class='rightCell'>```, which will contain the paragraph and kvp span for the text for Durham.

