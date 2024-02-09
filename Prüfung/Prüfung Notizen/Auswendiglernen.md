
# IPv4
## Netz Klassen
![[Netz Klassen.png]]

# IPv6
![[Pasted image 20240209115606.png]]
- **Priority**: Erlaubt das Setzen von Prioritäten. In dem 4-Bit-langen Feld kann die Quelle einzelnen Paketen Prioritäten relativ zu anderen Paketen zuweisen.
- **Flow Label**: Definiert eine Art Verbindungs-ID zwischen zwei Endpunkten. Router können anhand dieser Informationen Pakete, die zu einer Verbindung gehören, direkt übermitteln, ohne die übrigen Header-Informationen zu analysieren. Diese Funktion ist vor allem für Multimedia-Anwendungen interessant.
- **Payload Length**: Gibt die Länge des IPv6-Datenpakets als Integer-Wert an. Ist das Paket größer als 64 KByte, wird der Wert auf 0 gesetzt und die exakte Länge im Options-Header angegeben.
- **Next Header**: Gibt den Header-Typ an, der auf den IPv6-Header folgt, beispielsweise Routing- oder Options-Header.
- **Hop Limit**: Bestimmt die maximale Anzahl an Routern, die ein IPv6-Datenpaket überqueren kann, ähnlich dem Time-to-Live-Wert bei IPv4.
- **Source Address**: Gibt die 128-Bit-lange IP-Adresse des Senders an.
- **Destination Address**: Gibt die 128-Bit-lange IP-Adresse des Empfängers an.