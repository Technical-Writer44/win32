---
Description: 'The IRTC interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.'
ms.assetid: '9252a9ba-2c3e-40b9-b8de-84ef5d4831a7'
title: IRTC interface
---

# IRTC interface

The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network. **IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture. This interface includes a method that hands off a callback to the NPP.

## Members

The **IRTC** interface inherits from the [**IUnknown**](https://msdn.microsoft.com/library/windows/desktop/ms680509) interface. **IRTC** also has these types of members:

-   [Methods](#methods)

### Methods

The **IRTC** interface has these methods.



| Method                                                              | Description                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configure**](irtc-configure.md)                                 | Sets the trigger, pattern match, and buffer size of the capture.<br/>                                                                             |
| [**Connect**](irtc-connect.md)                                     | Connects the NPP to the network.<br/>                                                                                                             |
| [**Disconnect**](irtc-disconnect.md)                               | Disconnects the NPP from the network.<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | Retrieves the state of the [*capture*](c.md#-netmon-capture-gly), which indicates if the capture is running or paused.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Retrieves [*session*](s.md#-netmon-session-gly) and [*station information*](s.md#-netmon-station-information-gly) for the current capture.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Extracts time, buffer, driver, and other network statistics from the currently running capture.<br/>                                              |
| [**Pause**](irtc-pause.md)                                         | Temporarily stops the current capture.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Retrieves the status of the NPP.<br/>                                                                                                             |
| [**Resume**](irtc-resume.md)                                       | Restarts a paused capture.<br/>                                                                                                                   |
| [**Start**](irtc-start.md)                                         | Starts a capture.<br/>                                                                                                                            |
| [**Stop**](irtc-stop.md)                                           | Stops the current capture.<br/>                                                                                                                   |



�

## Requirements



|                                     |                                                                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�2000 Professional \[desktop apps only\]<br/>                                                                                               |
| Minimum supported server<br/> | Windows�2000 Server \[desktop apps only\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



�

�



