# DHCP-Server-Lab-1
Configuration of DHCP Server Lab 

English Versio
Project: Basic DHCP Configuration on Cisco Packet Tracer
This project demonstrates a basic configuration of DHCP (Dynamic Host Configuration Protocol) on a Cisco router using Cisco Packet Tracer. The goal is to set up a network where a router provides IP addresses to connected devices (PCs) automatically.

Network Topology
Router: Cisco ISR4321
Switch: 3650-24PS Multilayer Switch
PC: Connected to the switch via FastEthernet
Configuration Steps
Exclude IP Addresses

The router should not assign IP addresses in the range 10.1.1.1 to 10.1.1.100.
Command: ip dhcp excluded-address 10.1.1.1 10.1.1.100
Create DHCP Pool

Name: pc
Network: 10.1.1.0/24
Default Gateway: 10.1.1.1 (Router's IP address)
DNS Server: 10.1.1.1 (Router's IP address)

Commands:
ip dhcp pool pc
network 10.1.1.0 255.255.255.0
default-router 10.1.1.1
dns-server 10.1.1.1
Configure the Router's Interface

Assign IP address 10.1.1.1 to GigabitEthernet0/0/0 and enable the interface.

Commands:
interface GigabitEthernet0/0/0
ip address 10.1.1.1 255.255.255.0
no shutdown

Verify Configuration

Set the PC to use DHCP.
Test connectivity by pinging the router's IP address (10.1.1.1) from the PC.
Explanation of Key Concepts
DHCP: Automatically assigns IP addresses to devices.
IP Address: The unique address of a device in the network.
Gateway: The exit point of the network (Router1 in this case).
DNS Server: Translates domain names into IP addresses.
Ping: A tool used to test if a device is reachable.


Versione Italiana
Progetto: Configurazione Base DHCP su Cisco Packet Tracer
Questo progetto dimostra una configurazione base del DHCP (Dynamic Host Configuration Protocol) su un router Cisco utilizzando Cisco Packet Tracer. L'obiettivo è configurare una rete in cui un router fornisce automaticamente indirizzi IP ai dispositivi collegati (PC).

Topologia di Rete
Router: Cisco ISR4321
Switch: 3650-24PS Multilayer Switch
PC: Collegato allo switch tramite FastEthernet
Passaggi di Configurazione
Escludi gli Indirizzi IP

Il router non dovrebbe assegnare indirizzi IP nell'intervallo 10.1.1.1 - 10.1.1.100.
Comando: ip dhcp excluded-address 10.1.1.1 10.1.1.100
Crea un Pool DHCP

Nome: pc
Rete: 10.1.1.0/24
Gateway predefinito: 10.1.1.1 (Indirizzo IP del router)
Server DNS: 10.1.1.1 (Indirizzo IP del router)
Comandi:
ip dhcp pool pc
network 10.1.1.0 255.255.255.0
default-router 10.1.1.1
dns-server 10.1.1.1

Configura l'Interfaccia del Router
Assegna l'indirizzo IP 10.1.1.1 all'interfaccia GigabitEthernet0/0/0 e abilita l'interfaccia.
Comandi:
interface GigabitEthernet0/0/0
ip address 10.1.1.1 255.255.255.0
no shutdown

Verifica la Configurazione

Imposta il PC per utilizzare il DHCP.
Testa la connettività eseguendo il ping dell'indirizzo IP del router (10.1.1.1) dal PC.
Spiegazione dei Concetti Chiave
DHCP: Assegna automaticamente gli indirizzi IP ai dispositivi.
Indirizzo IP: L'indirizzo unico di un dispositivo nella rete.
Gateway: Il punto di uscita della rete (in questo caso il Router1).
Server DNS: Traduce i nomi di dominio in indirizzi IP.
Ping: Uno strumento utilizzato per verificare se un dispositivo è raggiungibile.
