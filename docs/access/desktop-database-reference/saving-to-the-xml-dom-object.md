---
title: Como salvar o objeto DOM XML
TOCTitle: Saving to the XML DOM object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95026d878270757c983e42164c92923570c898c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699909"
---
# <a name="saving-to-the-xml-dom-object"></a>Como salvar o objeto DOM XML

**Aplica-se a**: Access 2013, o Office 2013

## <a name="saving-to-the-xml-dom-object"></a>Salvando no objeto XML DOM

É possível salvar um **Recordset** em formato XML para uma instância de um objeto MSXML DOM, conforme mostrado no seguinte código Visual Basic:

```vb 
 
Dim xDOM As New MSXML.DOMDocument 
Dim rsXML As New ADODB.Recordset 
Dim sSQL As String, sConn As String 
     
sSQL = "SELECT customerid, companyname, contactname FROM customers" 
sConn="Provider=Microsoft.Jet.OLEDB.4.0;Data Source=D:\Program Files" & _ 
        "\Common Files\System\msadc\samples\NWind.mdb" 
rsXML.Open sSQL, sConn 
rsXML.Save xDOM, adPersistADO   'Save Recordset directly into a DOM tree. 
... 
```

