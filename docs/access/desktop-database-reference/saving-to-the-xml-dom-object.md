---
title: Salvando no objeto XML DOM
TOCTitle: Saving to the XML DOM Object
ms:assetid: 3c61fc30-9862-347b-c215-08597eccfead
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249160(v=office.15)
ms:contentKeyID: 48544318
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2bb85d34da052dda3e2bea5cead7ee4113ac2c12
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25461956"
---
# <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="6dd12-102">Salvando no objeto XML DOM</span><span class="sxs-lookup"><span data-stu-id="6dd12-102">Saving to the XML DOM Object</span></span>


<span data-ttu-id="6dd12-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dd12-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="saving-to-the-xml-dom-object"></a><span data-ttu-id="6dd12-104">Salvando no objeto XML DOM</span><span class="sxs-lookup"><span data-stu-id="6dd12-104">Saving to the XML DOM Object</span></span>

<span data-ttu-id="6dd12-105">É possível salvar um **Recordset** em formato XML para uma instância de um objeto MSXML DOM, conforme mostrado no seguinte código Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6dd12-105">You can save a **Recordset** in XML format to an instance of an MSXML DOM object, as shown in the following Visual Basic code:</span></span>

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

