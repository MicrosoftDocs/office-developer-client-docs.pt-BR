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
# <a name="cursortype-property-ado"></a><span data-ttu-id="7bd93-102">Propriedade CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="7bd93-102">CursorType property (ADO)</span></span>


<span data-ttu-id="7bd93-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bd93-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bd93-104">Indica o tipo do cursor utilizado em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="7bd93-104">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="7bd93-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7bd93-105">Settings and return values</span></span>

<span data-ttu-id="7bd93-106">Define ou retorna um valor [CursorTypeEnum](cursortypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="7bd93-106">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value.</span></span> <span data-ttu-id="7bd93-107">O valor padrão é **adOpenForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="7bd93-107">The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd93-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bd93-108">Remarks</span></span>

<span data-ttu-id="7bd93-109">Use a propriedade **CursorType** para especificar o tipo de cursor que deve ser usado ao abrir o objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="7bd93-109">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="7bd93-p102">Apenas uma definição de **adOpenStatic** terá suporte se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, não haverá erro; o **CursorType** com suporte mais próximo será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="7bd93-p102">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="7bd93-p103">Se um provedor não oferecer suporte ao tipo de cursor solicitado, ele poderá retornar um outro tipo. A propriedade **CursorType** será alterada para corresponder ao tipo de cursor real em uso quando o objeto [Recordset](recordset-object-ado.md) for aberto. Para verificar funcionalidades específicas do cursor que foi retornado, use o método [Supports](supports-method-ado.md). Depois de fechar o **Recordset**, a propriedade **CursorType** será revertida para sua definição original.</span><span class="sxs-lookup"><span data-stu-id="7bd93-p103">If a provider does not support the requested cursor type, it may return another cursor type. The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open. To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method. After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="7bd93-116">A planilha a seguir mostra as funcionalidades do provedor (identificadas por constantes do método **Supports** ) necessárias para cada tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="7bd93-116">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bd93-117">Para um Recordset deste CursorType</span><span class="sxs-lookup"><span data-stu-id="7bd93-117">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="7bd93-118">O método Supports deve retornar True para todas estas constantes</span><span class="sxs-lookup"><span data-stu-id="7bd93-118">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bd93-119"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-119"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd93-120">nenhum</span><span class="sxs-lookup"><span data-stu-id="7bd93-120">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd93-121"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-121"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd93-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-122"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bd93-123"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-123"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd93-124"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-124"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bd93-125"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-125"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="7bd93-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="7bd93-126"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="7bd93-p104">Embora **Supports** (**adUpdateBatch**) possa ser verdadeiro para cursores dinâmicos e somente de encaminhamento, para atualizações em lote você deve usar um cursor estático ou de conjunto de chaves. Defina a propriedade [LockType](locktype-property-ado.md) como **adLockBatchOptimistic** e a propriedade **CursorLocation** como **adUseClient** para habilitar o Cursor Service para OLE DB, necessário para as atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="7bd93-p104">Although **Supports**(**adUpdateBatch**) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor. Set the [LockType](locktype-property-ado.md) property to **adLockBatchOptimistic** and the **CursorLocation** property to **adUseClient** to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span>

<span data-ttu-id="7bd93-129">A propriedade **CursorType** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando ele estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="7bd93-129">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="7bd93-130">**Uso do Remote Data Service** Quando usada em um objeto Recordset do lado do cliente, a propriedade **CursorType** pode ser definida somente como **adOpenStatic**.</span><span class="sxs-lookup"><span data-stu-id="7bd93-130">**Remote Data Service Usage** When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

