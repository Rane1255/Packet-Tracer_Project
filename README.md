# MiniLab Réseau Cisco

# Objectif : Mettre en place une infrastructure réseau segmentée en VLANs :
- 1 routeur Cisco 1941
- 3 switches
- 3 bureaux (répartis sur les switchs)
- VLANs
- DHCP centralisé sur le routeur (fournir une attribution automatique des adresses IP via DHCP)
- Inter-VLAN routing
- Test de connectivité entre VLANs

# Equipements utilisés :
- routeur Cisco
- 3 switches (Switch PT puis migration vers 2960 pour confort de ports)
- 3 Access Points WI-FI
- 3 téléphones IP Cisco 7960
- 6 PC fixes
- 3 PC portables

# Configuration VLANs :
- VLAN 1 :  VoIP        |Réseau : 192.168.0.0/24
- VLAN 10 : PC fixes    |Réseau : 192.168.10.0/24
- VLAN 20 : Wi-Fi       |Réseau : 192.168.20.0/24
- VLAN 30 : Admin       |Réseau : 192.168.30.0/24
- VLAN 99 : native

# Configuration Switchs :
- Création des VLANs (1,10,20,30)
- Affectation des ports en mode access
- Configuration des liens trunk vers le routeur

# Configuration Routeur :
- VLAN 1 : g0/0.1
- VLAN 10 : g0/0.10
- VLAN 20 : g0/0.20
- VLAN 30 : g0/0.30
- Encapsulation dot1Q activée
- Routage inter-VLAN opérationnel

# DHCP
- Un pool DHCP par VLAN
- Attribution automatique des IP
- Passerelle par défaut configurée sur chaque VLAN

# NAT
- NAT overload configuré sur interface WAN
- ACL permettant le trafic des réseaux internes vers Internet
