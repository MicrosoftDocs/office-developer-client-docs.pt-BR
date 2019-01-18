---
title: Visual J++ (referência de banco de dados da área de trabalho do Access)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da13ae0f10e2338b961f2f12686bd378580a69d7
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705797"
---
# <a name="visual-j"></a><span data-ttu-id="dc4f8-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="dc4f8-102">Visual J++</span></span>


<span data-ttu-id="dc4f8-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc4f8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc4f8-104">Este pequeno exemplo do Microsoft Visual J++ mostra como você pode associar sua própria função a um evento específico.</span><span class="sxs-lookup"><span data-stu-id="dc4f8-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

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

<span data-ttu-id="dc4f8-105">Em primeiro lugar, o método de classe *onConnectionComplete* é associado ao evento **ConnectionComplete** criando um novo objeto **ConnectionEventHandler** e atribuindo a função *onConnectComplete* ao objeto.</span><span class="sxs-lookup"><span data-stu-id="dc4f8-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="dc4f8-106">A função *main* cria um objeto de **Conexão** e permite a manipulação de eventos, chamar o método **addOnConnectComplete** e passando-lhe o endereço da função *handler* .</span><span class="sxs-lookup"><span data-stu-id="dc4f8-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

