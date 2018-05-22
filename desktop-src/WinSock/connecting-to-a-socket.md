---
Description: 'For a client to communicate on a network, it must connect to a server.'
ms.assetid: 'fb52d2b7-70fa-497a-bbb4-42b25ea9d136'
title: Connecting to a Socket
---

# Connecting to a Socket

For a client to communicate on a network, it must connect to a server.

## To connect to a socket

Call the [**connect**](connect-2.md) function, passing the created socket and the [**sockaddr**](sockaddr-2.md) structure as parameters. Check for general errors.


```C++
// Connect to server.
iResult = connect( ConnectSocket, ptr->ai_addr, (int)ptr->ai_addrlen);
if (iResult == SOCKET_ERROR) {
    closesocket(ConnectSocket);
    ConnectSocket = INVALID_SOCKET;
}

// Should really try the next address returned by getaddrinfo
// if the connect call failed
// But for this simple example we just free the resources
// returned by getaddrinfo and print an error message

freeaddrinfo(result);

if (ConnectSocket == INVALID_SOCKET) {
    printf("Unable to connect to server!\n");
    WSACleanup();
    return 1;
}
```



The [**getaddrinfo**](getaddrinfo-2.md) function is used to determine the values in the [**sockaddr**](sockaddr-2.md) structure. In this example, the first IP address returned by the **getaddrinfo** function is used to specify the **sockaddr** structure passed to the [**connect**](connect-2.md). If the **connect** call fails to the first IP address, then try the next [**addrinfo**](addrinfo-2.md) structure in the linked list returned from the **getaddrinfo** function.

The information specified in the [**sockaddr**](sockaddr-2.md) structure includes:

-   the IP address of the server that the client will try to connect to.
-   the port number on the server that the client will connect to. This port was specified as port 27015 when the client called the [**getaddrinfo**](getaddrinfo-2.md) function.

Next Step: [Sending and Receiving Data on the Client](sending-and-receiving-data-on-the-client.md)

## Related topics

<dl> <dt>

[Getting Started With Winsock](getting-started-with-winsock.md)
</dt> <dt>

[Winsock Client Application](winsock-client-application.md)
</dt> <dt>

[Creating a Socket for the Client](creating-a-socket-for-the-client.md)
</dt> </dl>

 

 


