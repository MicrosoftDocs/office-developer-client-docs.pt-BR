---
title: Fabricando Recordsets Hierárquicos
TOCTitle: Fabricating Hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10f2eb3d46bc0091f8ebadb5c6aea6efe4eb6758
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881360"
---
# <a name="fabricating-hierarchical-recordsets"></a><span data-ttu-id="40adf-102">Fabricando Recordsets Hierárquicos</span><span class="sxs-lookup"><span data-stu-id="40adf-102">Fabricating Hierarchical Recordsets</span></span>


<span data-ttu-id="40adf-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="40adf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40adf-104">O exemplo a seguir mostra como fabricar um Recordset hierárquicosem uma fonte de dados base utilizando a gramática de formatação de dados para definir colunas para **Recordsets** pais, filhos e netos.</span><span class="sxs-lookup"><span data-stu-id="40adf-104">The following example shows how to fabricate a hierarchical Recordset without an underlying data source by using the data shaping grammar to define columns for parent, child, and grandchild **Recordsets**.</span></span>

<span data-ttu-id="40adf-p101">Para fabricar um **Recordset** hierárquico, é necessário especificar o Microsoft Data Shaping Service for OLE DB (MSDataShape) e você pode especificar o valor de Data Provider igual a NONE no parâmetro de sequência de conexão do método [Open](connection-object-ado.md) do objeto [Connection](open-method-ado-connection.md). Para obter mais informações, consulte [Provedores Necessários para Formação de Dados](required-providers-for-data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="40adf-p101">To fabricate a hierarchical **Recordset**, you must specify the Microsoft Data Shaping Service for OLE DB (MSDataShape), and you may specify a Data Provider value of NONE in the connection string parameter of the [Connection](connection-object-ado.md) object's [Open](open-method-ado-connection.md) method. For more information, see [Required Providers for Data Shaping](required-providers-for-data-shaping.md).</span></span>

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

<span data-ttu-id="40adf-107">Depois que o **Recordset** for fabricado, ele pode ser preenchido, manipulado ou persistido para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="40adf-107">After the **Recordset** has been fabricated, it can be populated, manipulated, or persisted to a file.</span></span>

