---
title: Visual J++ (referência de banco de dados da área de trabalho do Access)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d40a820b5ee3bd6e5c423cbb963a4514d4ff40e1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874542"
---
# <a name="visual-j"></a>Visual J++


**Aplica-se a**: Access 2013, o Office 2013

Este pequeno exemplo do Microsoft Visual J++ mostra como você pode associar sua própria função a um evento específico.

```java 
 
// BeginEventExampleVJ 
import com.ms.wfc.data.*; 
 
public class EventExampleVJ 
{ 
 ConnectionEventHandler handler = new ConnectionEventHandler(this,"onConnectComplete"); 
 
 public void onConnectComplete(Object sender,ConnectionEvent e) 
 { 
 if (e.adStatus == AdoEnums.EventStatus.ERRORSOCCURRED) 
 System.out.println("Connection failed"); 
 else 
 System.out.println("Connection completed"); 
 return; 
 } 
 
 public static void main (String[] args) 
 { 
 EventExampleVJ Class1 = new EventExampleVJ(); 
 Connection conn = new Connection(); 
 
 conn.addOnConnectComplete(Class1.handler); // Enable event support. 
 conn.open("DSN=Pubs"); 
 conn.close(); 
 conn.removeOnConnectComplete(Class1.handler); // Disable event support. 
 } 
} 
// EndEventExampleVJ 
```

Em primeiro lugar, o método de classe *onConnectionComplete* é associado ao evento **ConnectionComplete** criando um novo objeto **ConnectionEventHandler** e atribuindo a função *onConnectComplete* ao objeto.

A função *main* cria um objeto de **Conexão** e permite a manipulação de eventos, chamar o método **addOnConnectComplete** e passando-lhe o endereço da função *handler* .

