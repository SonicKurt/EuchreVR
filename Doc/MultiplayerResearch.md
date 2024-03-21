# Euchre with Friends Multiplayer Research

## Table of Contents
-[References](#references)

## Client and Server
Unreal Engine networking uses the client-server model. The server is the host of the game and holds the authoriative state of the game. The clients are remote-control Pawns that they own on the server. The server sends information about the game state to each client.

## Network Modes
Unreal Engine has four network modes: Standalone, Listen Server, Dedicated Server, and Client.

We should be using Listen Server for our game. We would allow to accept connections from remote clients and also allow local players to play on the server.

## Actor Replication
Unreal Engine replicates the state of actors to clients. The server is responsible for replicating the state of actors to clients. The server sends the state of actors to clients and the clients update the state of the actors.

## Network Role and Authority
Unreal Engine has two network roles: Authority and Simulated Proxy. The server has authority over all actors. The clients are simulated proxies of the actors. The server sends the state of the actors to the clients and the clients update the state of the actors.

## Meta Avatars
We cannot pull the avators from the Meta platform due to them not having an updated plugin to use with Unreal Engine 5. We will have to use the default avatars that come with Unreal Engine.

## References
[UE Forums - VR PC Multiplayer](https://forums.unrealengine.com/t/vr-pc-multiplayer/691364/2)
[Unreal Engine Networking and Multiplayer](https://dev.epicgames.com/documentation/en-us/unreal-engine/networking-and-multiplayer-in-unreal-engine?application_version=5.0)
[Unreal Engine Networking Overiew](https://dev.epicgames.com/documentation/en-us/unreal-engine/networking-overview-for-unreal-engine?application_version=5.0)
[Unreal Multiplayer Network Compendium](https://cedric-neukirchen.net/docs/multiplayer-compendium/introduction)