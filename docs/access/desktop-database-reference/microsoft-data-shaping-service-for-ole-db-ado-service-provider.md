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
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Service para OLE DB (Provedor de Serviços do ADO)


**Aplica-se a**: Access 2013 | Office 2013

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
<td><p>Indica se os objetos <strong>Recordset</strong> com valores duplicados para suas propriedades <strong>Reshape Name</strong> são permitidos. Se essa propriedade dinâmica for <strong>verdadeiro</strong> , e um novo <strong>conjunto de registros</strong> é criado com o mesmo especificado pelo usuário reshape nome como um <strong>Recordset</strong>de existente e nome de reshape do novo objeto <strong>Recordset</strong> é modificado para torná-lo exclusivo. Se essa propriedade for <strong>False</strong> e um novo <strong>conjunto de registros</strong> é criado com o mesmo especificado pelo usuário reshape nome como o <strong>conjunto de registros</strong>existente, ambos os objetos <strong>Recordset</strong> , terá a mesma a reshape nome. Portanto, nem <strong>Recordset</strong> pode ser reformatada desde que existam de ambos os conjuntos de registros. O valor padrão da propriedade é <strong>False</strong>.</p></td>
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

