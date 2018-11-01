---
title: Tutorial RDS (Visual J++)
TOCTitle: RDS Tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b01809cd17c9c1a5c1a73a5765bb8808692e4c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877916"
---
# <a name="rds-tutorial-visual-j"></a>Tutorial RDS (Visual J++)


**Aplica-se a**: Access 2013, o Office 2013

O ADO/WFC não segue completamente o modelo de objeto RDS porque não implementa o objeto [RDS.DataControl](datacontrol-object-rds.md). O ADO/WFC apenas implementa a classe do lado do cliente, [RDS.DataSpace](dataspace-object-rds.md).

A classe **DataSpace** implementa um método, [CreateObject](createobject-method-rds.md), que retorna um objeto [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)). A classe **DataSpace** também implementa a propriedade [InternetTimeout](internettimeout-property-rds.md).

A classe **ObjectProxy** implementa um método, call, que pode chamar qualquer objeto de negócios do lado do servidor.

**Esse é o início do tutorial.**

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```

**Esse é o fim do tutorial.**

