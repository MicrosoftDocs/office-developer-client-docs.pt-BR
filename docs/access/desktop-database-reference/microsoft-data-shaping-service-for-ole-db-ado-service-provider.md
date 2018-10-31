---
title: Microsoft Data Shaping Service para OLE DB (Provedor de Serviços do ADO)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 526c333f774aaf77079279932f8d9adf39915984
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861488"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="49965-102">Microsoft Data Shaping Service para OLE DB (Provedor de Serviços do ADO)</span><span class="sxs-lookup"><span data-stu-id="49965-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="49965-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="49965-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="49965-104">O Microsoft Data Shaping Service para provedor de serviços do OLE DB oferece suporte à construção de objetos [Recordset](recordset-object-ado.md) hierárquicos (formatados) a partir de um provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="49965-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="49965-105">Palavra-chave do provedor</span><span class="sxs-lookup"><span data-stu-id="49965-105">Provider Keyword</span></span>

<span data-ttu-id="49965-106">Para invocar o Data Shaping Service para OLE DB, especifique a palavra-chave e o valor a seguir na sequência de conexão.</span><span class="sxs-lookup"><span data-stu-id="49965-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="49965-107">Propriedades dinâmicas</span><span class="sxs-lookup"><span data-stu-id="49965-107">Dynamic Properties</span></span>

<span data-ttu-id="49965-108">Quando esse provedor de serviços é invocado, as propriedades dinâmicas abaixo são adicionadas à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="49965-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49965-109">Nome da propriedade dinâmica</span><span class="sxs-lookup"><span data-stu-id="49965-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="49965-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="49965-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49965-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="49965-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="49965-112">Indica se os objetos <strong>Recordset</strong> com valores duplicados para suas propriedades <strong>Reshape Name</strong> são permitidos.</span><span class="sxs-lookup"><span data-stu-id="49965-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="49965-113">Se essa propriedade dinâmica for <strong>verdadeiro</strong> , e um novo <strong>conjunto de registros</strong> é criado com o mesmo especificado pelo usuário reshape nome como um <strong>Recordset</strong>de existente e nome de reshape do novo objeto <strong>Recordset</strong> é modificado para torná-lo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="49965-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="49965-114">Se essa propriedade for <strong>False</strong> e um novo <strong>conjunto de registros</strong> é criado com o mesmo especificado pelo usuário reshape nome como o <strong>conjunto de registros</strong>existente, ambos os objetos <strong>Recordset</strong> , terá a mesma a reshape nome.</span><span class="sxs-lookup"><span data-stu-id="49965-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="49965-115">Portanto, nem <strong>Recordset</strong> pode ser reformatada desde que existam de ambos os conjuntos de registros.</span><span class="sxs-lookup"><span data-stu-id="49965-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="49965-116">O valor padrão da propriedade é <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="49965-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49965-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="49965-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="49965-p102">Indica o nome do provedor que fornecerá linhas para serem formatadas. Este valor pode ser NENHUM caso nenhum provedor seja utilizado para fornecer linhas.</span><span class="sxs-lookup"><span data-stu-id="49965-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="49965-p103">Você também pode definir propriedades dinâmicas que podem ser gravadas especificando seus nomes como palavras-chave na sequência de conexão. Por exemplo, no Microsoft Visual Basic, defina a propriedade dinâmica **Data Provider** como "MSDASQL", especificando:</span><span class="sxs-lookup"><span data-stu-id="49965-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="49965-p104">Além disso, você pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da propriedade [Properties](properties-collection-ado.md). Por exemplo, obtenha e imprima o valor atual da propriedade dinâmica **Data Provider** e defina um novo valor, como este:</span><span class="sxs-lookup"><span data-stu-id="49965-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="49965-124">Para obter mais informações sobre data shaping consulte [Data Shaping](data-shaping.md).</span><span class="sxs-lookup"><span data-stu-id="49965-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

