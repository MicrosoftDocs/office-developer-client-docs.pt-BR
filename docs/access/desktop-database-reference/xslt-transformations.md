---
title: Transformações XSLT
TOCTitle: XSLT Transformations
ms:assetid: 6a19310d-027f-e8d6-9859-0b545ae7e2f1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249418(v=office.15)
ms:contentKeyID: 48545425
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 733dd62122ee99d4e243c2af724f709a15333d51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463975"
---
# <a name="xslt-transformations"></a>Transformações XSLT


**Aplica-se a**: Access 2013 | Office 2013

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
