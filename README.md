# Cisco-Packet-Tracer

- ping Broadcast: 192.168.255.255

# Vorgehen
[Quelle](https://www.youtube.com/watch?v=MKY4Yu12wlo)
## Switch
- Vlan auf dem Switch erstellen
- Ports dem Vlan zuweisen
- Einen Port als Trunk zum Router konfigurieren

## Router
### Subinterfaces
Subinterface im Gigaport 0/0/0 erstellen
- interface Gigaport 0/0/0.1
- encapsulation dot1Q <Vlan-id>
- ip addres <ip für interface> (wird bei hosts als Gateway eingetragen)
- exit

