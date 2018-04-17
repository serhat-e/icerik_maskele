# icerik_maskele  / mask_content
> 02123332211 -> 021233***** <BR />
> KHJHJHKJHKHK -> KHJHJHK***** <br />

Karakter sayısı ve maskeleme sembolü parametre olarak gönderilebilir. <br />
Örneğin "Merhaba" kelimesini "Merh???" şeklinde göstermek için
```
icerik_maskele("Merhaba",3,"?")
```
şeklinde kullanılmalıdır.
<br />
```
function icerik_maskele($metin, $karakter_adet = 5, $sembol = "*") {
    if (strlen($metin) > $karakter_adet) {
        $a = substr($metin, 0, (int) -$karakter_adet);
        for ($i = 0; $i < $karakter_adet; $i++) {
            $a .= $sembol;
        }
        return $a;
    } else {
        return "";
    }
}
```
