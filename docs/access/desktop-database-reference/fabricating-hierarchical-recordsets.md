---
title: Fabricando Recordsets Hierárquicos
TOCTitle: Fabricating Hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81302ba1c18645a51913cb92179f4b61f3c32ce4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464513"
---
# <a name="fabricating-hierarchical-recordsets"></a>Fabricando Recordsets Hierárquicos


**Aplica-se a**: Access 2013 | Office 2013

O exemplo a seguir mostra como fabricar um Recordset hierárquicosem uma fonte de dados base utilizando a gramática de formatação de dados para definir colunas para **Recordsets** pais, filhos e netos.

Para fabricar um **Recordset** hierárquico, é necessário especificar o Microsoft Data Shaping Service for OLE DB (MSDataShape) e você pode especificar o valor de Data Provider igual a NONE no parâmetro de sequência de conexão do método [Open](connection-object-ado.md) do objeto [Connection](open-method-ado-connection.md). Para obter mais informações, consulte [Provedores Necessários para Formação de Dados](required-providers-for-data-shaping.md).

```vb
    Dim cn As New ADODB.Connection
    Dim rsCustomers As New ADODB.Recordset
    
    cn.Open "Provider=MSDataShape;Data Provider=NONE;"
     
    strShape = _
    "SHAPE APPEND NEW adInteger AS CustID," & _
                " NEW adChar(25) AS FirstName," & _
                " NEW adChar(25) AS LastName," & _
                " NEW adChar(12) AS SSN," & _
                " NEW adChar(50) AS Address," & _
             " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                            " NEW adInteger AS CustID," & _
                            " NEW adChar(20) AS BodyColor, " & _
                         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                                        " NEW adChar(20) AS Make, " & _
                                        " NEW adChar(20) AS Model," & _
                                        " NEW adChar(4) AS Year) " & _
                            " AS VINS RELATE VIN_NO TO VIN_NO))" & _
                " AS Vehicles RELATE CustID TO CustID) "
     
    rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1
```

Depois que o **Recordset** for fabricado, ele pode ser preenchido, manipulado ou persistido para um arquivo.
