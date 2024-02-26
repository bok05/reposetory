
# IPv4
## Netz Klassen
![[Netz Klassen.png]]

## Header
![[IPv4 Header.png]]
- **Version**: the first field tells us which IP version we are using, only IPv4 uses this header so you will always find decimal value 4 here.
- **Header Length**: this 4 bit field tells us the length of the IP header in 32 bit increments. The minimum length of an IP header is 20 bytes so with 32 bit increments, you would see value of 5 here. The maximum value we can create with 4 bits is 15 so with 32 bit increments, that would be a header length of 60 bytes. This field is also called the **Internet Header Length (IHL)**.
- **Type of Service**: this is used for QoS (Quality of Service). There are 8 bits that we can use to mark the packet which we can use to give the packet a certain treatment. You can read more about this field in my [IP precedence and DSCP lesson](https://networklessons.com/quality-of-service/ip-precedence-dscp-values/).
- **Total Length**: this 16-bit field indicates the entire size of the IP packet (header and data) in bytes. The minimum size is 20 bytes (if you have no data) and the maximum size is 65.535 bytes, that’s the highest value you can create with 16 bits.
- **Identification**: If the IP packet is fragmented then each fragmented packet will use the same 16 bit identification number to identify to which IP packet they belong to.
- **IP Flags**: These 3 bits are used for fragmentation:
    - The first bit is always set to 0.
    - The second bit is called the **DF (Don’t Fragment) bit** and indicates that this packet should not be fragmented.
    - The third bit is called the **MF (More Fragments)** bit and is set on all fragmented packets except the last one.
- **Fragment Offset**: this 13 bit field specifies the position of the fragment in the original fragmented IP packet.
- **Time to Live**: Everytime an IP packet passes through a router, the time to live field is decremented by 1. Once it hits 0 the router will drop the packet and sends an ICMP time exceeded message to the sender. The time to live field has 8 bits and is used to prevent packets from looping around forever (if you have a routing loop).
- **Protocol**: this 8 bit field tells us which protocol is enapsulated in the IP packet, for example TCP has value 6 and UDP has value 17.
- **Header Checksum**: this 16 bit field is used to store a checksum of the header. The receiver can use the checksum to check if there are any errors in the header.
- **Source Address**: here you will find the 32 bit source IP address.
- **Destination Address**: and here’s the 32 bit destination IP address.
- **IP Option**: this field is not used often, is optional and has a variable length based on the options that were used. When you use this field, the value in the header length field will increase. An example of a possible option is “source route” where the sender requests for a certain routing path.

# IPv6

## Header
![[IPv6 Header.png]]
- **Traffic Class**: Der Wert des Feldes definiert die Priorität des Paketes.
- **Flow Label**: Definiert eine Art Verbindungs-ID zwischen zwei Endpunkten. Router können anhand dieser Informationen Pakete, die zu einer Verbindung gehören, direkt übermitteln, ohne die übrigen Header-Informationen zu analysieren. Diese Funktion ist vor allem für Multimedia-Anwendungen interessant.
- **Payload Length**: Gibt die Länge des IPv6-Datenpakets als Integer-Wert an. Ist das Paket größer als 64 KByte, wird der Wert auf 0 gesetzt und die exakte Länge im Options-Header angegeben.
- **Next Header**: Gibt den Header-Typ an, der auf den IPv6-Header folgt, beispielsweise Routing- oder Options-Header.
- **Hop Limit**: Bestimmt die maximale Anzahl an Routern, die ein IPv6-Datenpaket überqueren kann, ähnlich dem Time-to-Live-Wert bei IPv4.
- **Source Address**: Gibt die 128-Bit-lange IP-Adresse des Senders an.
- **Destination Address**: Gibt die 128-Bit-lange IP-Adresse des Empfängers an.
-

## Netzplan


![[Pasted image 20240215133706.png]]

