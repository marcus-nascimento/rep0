# rep0
My first repo
====

Isto é um `teste` [testando] testando link (http://git.tst.jus.br/juridico/esij/blob/master/src/main/java/br/gov/tst/ajudante/PautaComparator.java)

```javascript
$(function(){
  $('div').html('I am a div.');
});
```

```java
public int compare(Pauta p1, Pauta p2) {
    if (p1.getId().getAnoPauta().shortValue() > p2.getId().getAnoPauta().shortValue() ) {
        return 1;
    } else if (p1.getId().getAnoPauta().shortValue() < p2.getId().getAnoPauta().shortValue() ) {
        return -1;
    } else if (p1.getId().getAnoPauta().shortValue() == p2.getId().getAnoPauta().shortValue()){
        // num pauta
        if (p1.getId().getNumPauta().shortValue() > p2.getId().getNumPauta().shortValue() ) {
            return 1;
        } else if (p1.getId().getNumPauta().shortValue() < p2.getId().getNumPauta().shortValue() ) {
            return -1;
        } else if (p1.getId().getNumPauta().shortValue() == p2.getId().getNumPauta().shortValue()){
            // tipo sessÃ£o
            if (p1.getId().getTipSessao().equalsIgnoreCase("E")
                    && p2.getId().getTipSessao().equalsIgnoreCase("O")) {
                return 1;
            } else if (p1.getId().getTipSessao().equalsIgnoreCase("O")
                    && p2.getId().getTipSessao().equalsIgnoreCase("E")) {
                return -1;
            } else {
                return 0;
            }
        }
    }
    return 0;
}
```

Teste testando
-------------------------------

```java
/**
 * PautaComparator pode ser usada para ordenar pautas primeiro pelo ano,
 * depois pelo número e por último pelo tipo de sessão.
 */
@Test
public void ordenaPautasPorAnoNumeroTipoSessao() {
    List<Pauta> pautas = criaLista(
        new PautaId(null, Short.valueOf("2016"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2016"), Short.valueOf("1"), "E"),
        new PautaId(null, Short.valueOf("2015"), Short.valueOf("2"), "O"),
        new PautaId(null, Short.valueOf("2015"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2013"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2012"), Short.valueOf("1"), "O")
    );
    List<Pauta> ordenada = criaLista(
        new PautaId(null, Short.valueOf("2012"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2013"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2015"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2015"), Short.valueOf("2"), "O"),
        new PautaId(null, Short.valueOf("2016"), Short.valueOf("1"), "O"),
        new PautaId(null, Short.valueOf("2016"), Short.valueOf("1"), "E")
    );
    Collections.sort(pautas, new PautaComparator());
    assertEquals(ordenada, pautas);
}

private List<Pauta> criaLista(PautaId... ids) {
    final List<Pauta> pautas = new ArrayList<Pauta>();
    for (PautaId id : ids) {
        pautas.add(new Pauta(id, null, null));
    }
    return pautas;
}
```

Mais um teste
-------------------


### Outro teste
`testando`
[testando]
1. teste
2. teste

