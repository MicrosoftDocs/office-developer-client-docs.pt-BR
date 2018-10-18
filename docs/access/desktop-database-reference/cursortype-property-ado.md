---
<span data-ttu-id="aac41-101"><<<<<<< Título cabeça: propriedade CursorType (ADO) TOCTitle: propriedade CursorType (ADO) === título: propriedade CursorType (ADO) TOCTitle: propriedade CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="aac41-101"><<<<<<< HEAD title: CursorType Property (ADO) TOCTitle: CursorType Property (ADO) ======= title: CursorType property (ADO) TOCTitle: CursorType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aac41-102">ms:assetid de mestre: f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID: ms.date 48548682: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="aac41-102">master ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID: 48548682 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="aac41-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="aac41-103"><<<<<<< HEAD</span></span>
# <a name="cursortype-property-ado"></a><span data-ttu-id="aac41-104">Propriedade CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="aac41-104">CursorType Property (ADO)</span></span>
=======
# <a name="cursortype-property-ado"></a><span data-ttu-id="aac41-105">Propriedade CursorType (ADO)</span><span class="sxs-lookup"><span data-stu-id="aac41-105">CursorType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aac41-106">mestre</span><span class="sxs-lookup"><span data-stu-id="aac41-106">master</span></span>


<span data-ttu-id="aac41-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aac41-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aac41-108">Indica o tipo do cursor utilizado em um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="aac41-108">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="aac41-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="aac41-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="aac41-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="aac41-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="aac41-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aac41-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="aac41-112">mestre</span><span class="sxs-lookup"><span data-stu-id="aac41-112">master</span></span>

<span data-ttu-id="aac41-p101">Define ou retorna um valor [CursorTypeEnum](cursortypeenum.md). O valor padrão é **adOpenForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="aac41-p101">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value. The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aac41-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aac41-115">Remarks</span></span>

<span data-ttu-id="aac41-116">Use a propriedade **CursorType** para especificar o tipo de cursor que deve ser usado ao abrir o objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="aac41-116">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="aac41-p102">Apenas uma definição de **adOpenStatic** terá suporte se a propriedade [CursorLocation](cursorlocation-property-ado.md) for definida como **adUseClient**. Se um valor sem suporte for definido, não haverá erro; o **CursorType** com suporte mais próximo será usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="aac41-p102">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="aac41-p103">Se um provedor não oferecer suporte ao tipo de cursor solicitado, ele poderá retornar um outro tipo. A propriedade **CursorType** será alterada para corresponder ao tipo de cursor real em uso quando o objeto [Recordset](recordset-object-ado.md) for aberto. Para verificar funcionalidades específicas do cursor que foi retornado, use o método [Supports](supports-method-ado.md). Depois de fechar o **Recordset**, a propriedade **CursorType** será revertida para sua definição original.</span><span class="sxs-lookup"><span data-stu-id="aac41-p103">If a provider does not support the requested cursor type, it may return another cursor type. The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open. To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method. After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="aac41-123">A planilha a seguir mostra as funcionalidades do provedor (identificadas por constantes do método **Supports** ) necessárias para cada tipo de cursor.</span><span class="sxs-lookup"><span data-stu-id="aac41-123">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aac41-124">Para um Recordset deste CursorType</span><span class="sxs-lookup"><span data-stu-id="aac41-124">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="aac41-125">O método Supports deve retornar True para todas estas constantes</span><span class="sxs-lookup"><span data-stu-id="aac41-125">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aac41-126"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-126"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="aac41-127">nenhum</span><span class="sxs-lookup"><span data-stu-id="aac41-127">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac41-128"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-128"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="aac41-129"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-129"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac41-130"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-130"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="aac41-131"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-131"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac41-132"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-132"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="aac41-133"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="aac41-133"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="aac41-p104">Embora <STRONG>Supports</STRONG> (<STRONG>adUpdateBatch</STRONG>) possa ser verdadeiro para cursores dinâmicos e somente de encaminhamento, para atualizações em lote você deve usar um cursor estático ou de conjunto de chaves. Defina a propriedade <A href="locktype-property-ado.md">LockType</A> como <STRONG>adLockBatchOptimistic</STRONG> e a propriedade <STRONG>CursorLocation</STRONG> como <STRONG>adUseClient</STRONG> para habilitar o Cursor Service para OLE DB, necessário para as atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="aac41-p104">Although <STRONG>Supports</STRONG>(<STRONG>adUpdateBatch</STRONG>) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor. Set the <A href="locktype-property-ado.md">LockType</A> property to <STRONG>adLockBatchOptimistic</STRONG> and the <STRONG>CursorLocation</STRONG> property to <STRONG>adUseClient</STRONG> to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span></P>



<span data-ttu-id="aac41-136">A propriedade **CursorType** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando ele estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="aac41-136">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="aac41-137">**Uso de serviço de dados remotos** Quando usado em um objeto Recordset do lado do cliente, a propriedade **CursorType** pode ser definida apenas como **adOpenStatic**.</span><span class="sxs-lookup"><span data-stu-id="aac41-137">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

