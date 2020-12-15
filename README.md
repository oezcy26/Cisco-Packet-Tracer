# Cisco-Packet-Tracer

- ping Broadcast: 192.168.255.255

# VLAN.pkt
Es sollen VLANS auf einem Switch erstellt werden, welche beim Router verbunden sind.

## Switch
Wechsel in den Config-Mode: `configure terminal`
Einzelne Untermenüs schliessen: `exit`

- Vlan auf dem Switch erstellen:
  - `vlan database`
  - `vlan <vlanId> name rot`
- Interface/Port dem Vlan zuweisen
  - `interface <Iface-name>`
  - `switchport access vlan <vlanId>`
- Einen Port als Trunk zum Router konfigurieren. Es soll allen VLAN's erlaubt sein, den Trunk zu nutzen.
  - `interface <Iface-name>`
  - `switchport mode trunk` : Versetzt das interface in den Trunk-Mode für alle VLAN's
  - `switchport trunk allowed vlan add <VlanId>` : Einzelnde VlanId's dem Trunk zuweisen.

## Router
### Subinterfaces
Subinterface im Gigaport 0/0/0 erstellen, geht nur mit dem CLI
- `interface Gigaport 0/0/0.1` : für erstes Subinterface auf Port 0/0/0
- `encapsulation dot1Q 2` : die 2 mit der VlanId ersetzen
- `ip addres 192.168.1.1 255.255.255.0` : Setzen der IP fürs Subinterface  
Diese IP Adresse muss bei den Host's als Gateway konfiguriert werden.
- `exit`

## Hilfestellungen
- [Video: Vlan mit Packet-Tracer](https://www.youtube.com/watch?v=MKY4Yu12wlo)
- [Manual pdf](https://www.cisco.com/c/en/us/td/docs/routers/ncs6000/software/interfaces/command/reference/b-interfaces-cr-ncs6k/b_interfaces_cr50ncs_chapter_01001.pdf)

# Statisches Routing
2 Netzwerke, verbunden mit einem Zwischennetzwerk. 
