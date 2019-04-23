---
title: Microsoft Data Shaping Service para OLE DB (Provedor de Serviços do ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288957"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="ba687-102">Microsoft Data Shaping Service para OLE DB (Provedor de serviços ADO)</span><span class="sxs-lookup"><span data-stu-id="ba687-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="ba687-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ba687-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ba687-104">O Microsoft Data Shaping Service para provedor de serviços do OLE DB oferece suporte à construção de objetos [Recordset](recordset-object-ado.md) hierárquicos (formatados) a partir de um provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="ba687-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="ba687-105">Palavra-chave do provedor</span><span class="sxs-lookup"><span data-stu-id="ba687-105">Provider Keyword</span></span>

<span data-ttu-id="ba687-106">Para invocar o Data Shaping Service para OLE DB, especifique a palavra-chave e o valor a seguir na sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="ba687-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="ba687-107">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="ba687-107">Dynamic Properties</span></span>

<span data-ttu-id="ba687-108">Quando esse provedor de serviços é invocado, as propriedades dinâmicas abaixo são adicionadas à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ba687-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ba687-109">Nome da propriedade dinâmica</span><span class="sxs-lookup"><span data-stu-id="ba687-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="ba687-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba687-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ba687-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="ba687-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="ba687-112">Indica se objetos <strong>Recordset</strong> com valores duplicados nas suas propriedades <strong>Reshape Name</strong> são permitidos.</span><span class="sxs-lookup"><span data-stu-id="ba687-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="ba687-113">Se o valor desta propriedade dinâmica for <strong>True</strong> e um novo <strong>Recordset</strong> for criado com o mesmo nome de reformatação, especificado pelo usuário, de um <strong>Recordset</strong> existente, o nome de reformatação do novo objeto <strong>Recordset</strong> será modificado para tornar-se único.</span><span class="sxs-lookup"><span data-stu-id="ba687-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="ba687-114">Se o valor desta propriedade for <strong>False</strong> e um novo <strong>Recordset</strong> for criado com o mesmo nome de reformatação, especificado pelo usuário, de um <strong>Recordset</strong> existente, ambos os objetos <strong>Recordset</strong> terão o mesmo nome de reformatação.</span><span class="sxs-lookup"><span data-stu-id="ba687-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="ba687-115">Portanto, nenhum dos dois poderá ser reformatado enquanto ambos os objetos <strong>Recordset</strong> existirem.</span><span class="sxs-lookup"><span data-stu-id="ba687-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="ba687-116">O valor padrão da propriedade é <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="ba687-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ba687-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="ba687-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="ba687-p102">Indica o nome do provedor que fornecerá linhas para serem formatadas. Este valor pode ser NENHUM caso nenhum provedor seja utilizado para fornecer linhas.</span><span class="sxs-lookup"><span data-stu-id="ba687-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ba687-p103">Você também pode definir propriedades dinâmicas que podem ser gravadas especificando seus nomes como palavras-chave na sequência de conexão. Por exemplo, no Microsoft Visual Basic, defina a propriedade dinâmica **Data Provider** como "MSDASQL", especificando:</span><span class="sxs-lookup"><span data-stu-id="ba687-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="ba687-p104">Além disso, você pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da propriedade [Properties](properties-collection-ado.md). Por exemplo, obtenha e imprima o valor atual da propriedade dinâmica **Data Provider** e defina um novo valor, como este:</span><span class="sxs-lookup"><span data-stu-id="ba687-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="ba687-124">Para obter mais informações sobre data shaping consulte [Data Shaping](data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="ba687-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

