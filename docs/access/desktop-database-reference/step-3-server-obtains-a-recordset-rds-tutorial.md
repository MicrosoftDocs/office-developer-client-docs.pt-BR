---
title: 'Etapa 3: O servidor obtém um Recordset (tutorial RDS)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddd306e95ccf9ed68848b516c6d23d45286edf63
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943833"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>Etapa 3: O servidor obtém um Recordset (Tutorial RDS)

**Aplica-se a**: Access 2013, o Office 2013

O programa do servidor usa a sequência de conexão e o texto de comando para consultar a fonte de dados para as linhas desejadas. O ADO geralmente é usado para recuperar esse **Recordset**, embora outras interfaces de acesso a dados da Microsoft, como o OLE DB, podem ser usadas.

Um programa de servidor personalizado pode parecer com:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

