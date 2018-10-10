---
title: 'Etapa 4: O servidor retorna o Recordset (Tutorial RDS)'
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41fd4a1aabda0887d265e3aa0ec9201b1abbbde7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465080"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a>Etapa 4: O servidor retorna o Recordset (Tutorial RDS)


**Aplica-se a**: Access 2013 | Office 2013

O RDS converte o objeto **Recordset** recuperado para um formato que pode ser enviado de volta ao cliente (ou seja, ele *empacota* o **Recordset**). O formato exato da conversão e como ele é gasto depende de o servidor estar na Internet ou na intranet, uma rede local ou é uma biblioteca de vínculos dinâmicos. Contudo, este detalhe não é crítico; o que importa é que o RDS envia o **Recordset** de volta ao cliente.

No lado cliente, um objeto **Recordset** é retornado e atribuído a uma variável local.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

