---
title: Transformações XSLT
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7120ec08a6a222293fc53c5a98f62c50fd5b3621
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722596"
---
# <a name="xslt-transformations"></a>Transformações de XSLT


**Aplica-se a**: Access 2013, o Office 2013

## <a name="xslt-transformations"></a>Transformações XSLT

O XSLT pode ser aplicado ao XML gerado para transformá-lo em outro formato. O entendimento do formato XML no ADO ajuda no desenvolvimento de modelos XSLT que podem ser transformá-lo em um formato mais amigável.

Por exemplo, você sabe que cada linha do **Recordset** é salva como o elemento z:row dentro do elemento rs:data. Da mesma forma, cada campo do **Recordset** é salvo como um par atributo-valor para este elemento.

O seguinte script XSLT pode ser aplicado ao XML mostrado na seção anterior para transformá-lo em uma tabela HTML a ser exibida no navegador:

```xml 
 
<?xml version="1.0" encoding="ISO-8859-1"?> 
<html xmlns:xsl="https://www.w3.org/TR/WD-xsl"> 
<body STYLE="font-family:Arial, helvetica, sans-serif; font-size:12pt; background-color:white"> 
<table border="1" style="table-layout:fixed" width="600"> 
  <col width="200"></col> 
  <tr bgcolor="teal"> 
    <th><font color="white">CustomerId</font></th> 
    <th><font color="white">CompanyName</font></th> 
    <th><font color="white">ContactName</font></th> 
  </tr> 
<xsl:for-each select="xml/rs:data/z:row"> 
  <tr bgcolor="navy"> 
    <td><font color="white"><xsl:value-of select="@CustomerID"/></font></td> 
    <td><font color="white"><xsl:value-of select="@CompanyName"/></font></td> 
    <td><font color="white"><xsl:value-of select="@ContactName"/></font></td>  
  </tr> 
</xsl:for-each> 
</table> 

</body> 
</html> 
```

O XSLT converte o fluxo XML gerado pelo método **Save** do ADO em uma tabela HTML que exibe cada campo do **Recordset** junto com um cabeçalho de tabela. Aos cabeçalhos e linhas da tabela também são atribuídas fontes e cores diferentes.

