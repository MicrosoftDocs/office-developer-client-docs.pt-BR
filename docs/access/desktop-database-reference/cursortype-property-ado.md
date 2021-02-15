---
title: Propriedade CursorType (ADO)
TOCTitle: CursorType property (ADO)
ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15)
ms:contentKeyID: 48548682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7cdb32bb8ff9bb6e0556a87de0efe82cd919dbe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295181"
---
# <a name="cursortype-property-ado"></a>Propriedade CursorType (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o tipo do cursor utilizado em um objeto [Recordset](recordset-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um valor [CursorTypeEnum](cursortypeenum.md). O valor padrão é **adOpenForwardOnly**.

## <a name="remarks"></a>Comentários

Use a propriedade **CursorType** para especificar o tipo de cursor que deve ser usado ao abrir o objeto **Recordset**.

Apenas uma definição de **adOpenStatic** terá suporte se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, não haverá erro; o **CursorType** com suporte mais próximo será usado em seu lugar.

Se um provedor não oferecer suporte ao tipo de cursor solicitado, ele poderá retornar um outro tipo. A propriedade **CursorType** será alterada para corresponder ao tipo de cursor real em uso quando o objeto [Recordset](recordset-object-ado.md) for aberto. Para verificar funcionalidades específicas do cursor que foi retornado, use o método [Supports](supports-method-ado.md). Depois de fechar o **Recordset**, a propriedade **CursorType** será revertida para sua definição original.

A planilha a seguir mostra as funcionalidades do provedor (identificadas por constantes do método **Supports** ) necessárias para cada tipo de cursor.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Para um Recordset deste CursorType</p></th>
<th><p>O método Supports deve retornar True para todas estas constantes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>nenhum</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> Embora **Supports** (**adUpdateBatch**) possa ser verdadeiro para cursores dinâmicos e somente de encaminhamento, para atualizações em lote você deve usar um cursor estático ou de conjunto de chaves. Defina a propriedade [LockType](locktype-property-ado.md) como **adLockBatchOptimistic** e a propriedade **CursorLocation** como **adUseClient** para habilitar o Cursor Service para OLE DB, necessário para as atualizações em lote.

A propriedade **CursorType** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando ele estiver aberto.

**Uso do Remote Data Service** Quando usada em um objeto Recordset do lado do cliente, a propriedade **CursorType** pode ser definida somente como **adOpenStatic**.

