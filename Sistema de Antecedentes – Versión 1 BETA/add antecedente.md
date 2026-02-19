# Es un comando de slash /addantecedente


```

$nomention
$var[userID;$findUser[$message[1;usuario];no]]
$var[motivo;$message[motivo]]


$jsonParse[$getUserVar[antecedentes;$var[userID]]]
$jsonSetString[cntAnt;$if[$jsonExists[cntAnt]==true] $sum[$json[cntAnt];1] $else 1 $endif]
$jsonSetString[$json[cntAnt];date;$getTimestamp]
$jsonSetString[$json[cntAnt];reason;$var[motivo]]
$jsonSetString[$json[cntAnt];mod;$authorID]
$setUserVar[antecedentes;$jsonStringify;$var[userID]]

$color[1F1F1F]
$title[Registro de Antecedente Penal]

$description[
~~‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ~~‎
**Ciudadano:** <@$var[userID]>  
**Motivo:** 
$var[motivo]
~~‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ~~‎
**Oficial:** <@$authorID>  
**Fecha:** <t:$getTimestamp:f>  

**Expediente Nº:** `$json[cntAnt]/10`
]
$color[1F3A5F]
$footer[Wizard RP • Sistema Judicial]
$thumbnail[https://i.imgur.com/E7aRQ5i.png]
```
