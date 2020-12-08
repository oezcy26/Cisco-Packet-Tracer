# Cisco-Packet-Tracer

- ping Broadcast: 192.168.255.255

# VLAN.pkt
Es sollen VLANS auf einem Switch erstellt werden, welche beim Router verbunden sind.

## Switch
- Vlan auf dem Switch erstellen
- Ports dem Vlan zuweisen
- Einen Port als Trunk zum Router konfigurieren. Es soll allen VLAN's erlaubt sein, den Trunk zu nutzen.

## Router
### Subinterfaces
Subinterface im Gigaport 0/0/0 erstellen, geht nur mit dem CLI
- `interface Gigaport 0/0/0.1` : für erstes Subinterface auf Port 0/0/0
- `encapsulation dot1Q 2` : die 2 mit der VlanId ersetzen
- `ip addres 192.168.1.1 255.255.255.0` : Setzen der IP fürs Subinterface
- `exit`
Diese IP Adresse muss bei den Host's als Gateway konfiguriert werden.

## Hilfestellungen
- [Video: Vlan mit Packet-Tracer](https://www.youtube.com/watch?v=MKY4Yu12wlo)
- [Manual pdf](https://www.cisco.com/c/en/us/td/docs/routers/ncs6000/software/interfaces/command/reference/b-interfaces-cr-ncs6k/b_interfaces_cr50ncs_chapter_01001.pdf)

