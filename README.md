# StreamDivert
StreamDivert is a tool to man-in-the-middle or relay in and outgoing network connections on a system. It has the ability to, for example, relay all incoming SMB connections to port 445 to another server, or only relay specific incoming SMB connections from a specific set of source IP's to another server. Summed up, StreamDivert is able to:


*  Relay all incoming connections to a specific port to another destination.
*  Relay incoming connections from a specific source IP to a port to another destination.
*  Relay all outgoing connections to a specific port to another destination.
*  Relay outgoing connections to a specific IP and port to another destination.
*  Handle IPv4 and IPv6 connections.
*  Handle TCP, UDP and ICMP connections

## Download Binaries
Pre-compiled binaries for StreamDivert can be downloaded [here](url).

## Usage
How do you use StreamDivert? Run the the tool:

```console
streamdivert.exe [config file]
```

The config file contains entries for streams you want to have diverted. En example config file:
```conf
//Divert all inbound connections to port 445 (SMB) coming from 10.0.1.50 to 10.0.1.49 port 445
tcp < 445 10.0.1.50 -> 10.0.1.49 445

//Divert all inbound connections to port 445 (SMB) to 10.0.1.48 port 445
tcp < 445 0.0.0.0 -> 10.0.1.48 445

//
tcp < 445 fe80::f477:846a:775d:d37 -> fe80::20c:29ff:fe6f:88ff 445
```

## Contributing to Streamdivert
Features wanted:
*  IP range support
*  ...