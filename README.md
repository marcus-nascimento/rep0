# rep0
My first repo

Isto é um `teste` [testando]

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

