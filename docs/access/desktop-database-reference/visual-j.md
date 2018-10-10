---
title: Visual J++ (referência de banco de dados da área de trabalho do Access)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bc76026fb5b5b426b41c8334bc61d5b9485dd76
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463586"
---
# <a name="visual-j"></a><span data-ttu-id="81681-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="81681-102">Visual J++</span></span>


<span data-ttu-id="81681-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="81681-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="81681-104">Este pequeno exemplo do Microsoft Visual J++ mostra como você pode associar sua própria função a um evento específico.</span><span class="sxs-lookup"><span data-stu-id="81681-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

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

<span data-ttu-id="81681-105">Em primeiro lugar, o método de classe *onConnectionComplete* é associado ao evento **ConnectionComplete** criando um novo objeto **ConnectionEventHandler** e atribuindo a função *onConnectComplete* ao objeto.</span><span class="sxs-lookup"><span data-stu-id="81681-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="81681-106">A função *main* cria um objeto de **Conexão** e permite a manipulação de eventos, chamar o método **addOnConnectComplete** e passando-lhe o endereço da função *handler* .</span><span class="sxs-lookup"><span data-stu-id="81681-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

