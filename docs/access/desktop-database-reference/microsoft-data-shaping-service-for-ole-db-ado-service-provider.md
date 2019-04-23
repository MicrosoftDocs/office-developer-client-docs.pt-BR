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
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Service para OLE DB (Provedor de serviços ADO)


**Aplica-se ao:** Access 2013, Office 2013

O Microsoft Data Shaping Service para provedor de serviços do OLE DB oferece suporte à construção de objetos [Recordset](recordset-object-ado.md) hierárquicos (formatados) a partir de um provedor de dados.

## <a name="provider-keyword"></a>Palavra-chave do provedor

Para invocar o Data Shaping Service para OLE DB, especifique a palavra-chave e o valor a seguir na sequência de conexão.

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>Propriedades dinâmicas

Quando esse provedor de serviços é invocado, as propriedades dinâmicas abaixo são adicionadas à coleção [Properties](connection-object-ado.md) do objeto [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome da propriedade dinâmica</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Unique Reshape Names</strong></p></td>
<td><p>Indica se objetos <strong>Recordset</strong> com valores duplicados nas suas propriedades <strong>Reshape Name</strong> são permitidos. Se o valor desta propriedade dinâmica for <strong>True</strong> e um novo <strong>Recordset</strong> for criado com o mesmo nome de reformatação, especificado pelo usuário, de um <strong>Recordset</strong> existente, o nome de reformatação do novo objeto <strong>Recordset</strong> será modificado para tornar-se único. Se o valor desta propriedade for <strong>False</strong> e um novo <strong>Recordset</strong> for criado com o mesmo nome de reformatação, especificado pelo usuário, de um <strong>Recordset</strong> existente, ambos os objetos <strong>Recordset</strong> terão o mesmo nome de reformatação. Portanto, nenhum dos dois poderá ser reformatado enquanto ambos os objetos <strong>Recordset</strong> existirem. O valor padrão da propriedade é <strong>False</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Provider</strong></p></td>
<td><p>Indica o nome do provedor que fornecerá linhas para serem formatadas. Este valor pode ser NENHUM caso nenhum provedor seja utilizado para fornecer linhas.</p></td>
</tr>
</tbody>
</table>


Você também pode definir propriedades dinâmicas que podem ser gravadas especificando seus nomes como palavras-chave na sequência de conexão. Por exemplo, no Microsoft Visual Basic, defina a propriedade dinâmica **Data Provider** como "MSDASQL", especificando:

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

Além disso, você pode definir ou recuperar uma propriedade dinâmica especificando o seu nome como índice da propriedade [Properties](properties-collection-ado.md). Por exemplo, obtenha e imprima o valor atual da propriedade dinâmica **Data Provider** e defina um novo valor, como este:

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

Para obter mais informações sobre data shaping consulte [Data Shaping](data-shaping.md).

