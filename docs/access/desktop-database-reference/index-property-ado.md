---
<span data-ttu-id="c6961-101"><<<<<<< Título cabeça: TOCTitle da propriedade Index (ADO): propriedade Index (ADO) === título: propriedade (ADO) Index TOCTitle: índice de propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="c6961-101"><<<<<<< HEAD title: Index Property (ADO) TOCTitle: Index Property (ADO) ======= title: Index property (ADO) TOCTitle: Index property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c6961-102">ms:assetid de mestre: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15) ms:contentKeyID: ms.date 48544715: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c6961-102">master ms:assetid: 4cc00521-dcb4-19b2-2174-6e0e9bd42e62 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249241(v=office.15) ms:contentKeyID: 48544715 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c6961-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c6961-103"><<<<<<< HEAD</span></span>
# <a name="index-property-ado"></a><span data-ttu-id="c6961-104">Propriedade Index (ADO)</span><span class="sxs-lookup"><span data-stu-id="c6961-104">Index Property (ADO)</span></span>
=======
# <a name="index-property-ado"></a><span data-ttu-id="c6961-105">Propriedade Index (ADO)</span><span class="sxs-lookup"><span data-stu-id="c6961-105">Index property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c6961-106">mestre</span><span class="sxs-lookup"><span data-stu-id="c6961-106">master</span></span>


<span data-ttu-id="c6961-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6961-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c6961-108">Indica o nome do índice que está atualmente em vigor para um objeto [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6961-108">Indicates the name of the index currently in effect for a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="c6961-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c6961-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="c6961-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c6961-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="c6961-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c6961-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="c6961-112">mestre</span><span class="sxs-lookup"><span data-stu-id="c6961-112">master</span></span>

<span data-ttu-id="c6961-113">Define ou retorna um valor **String**, que é o nome do índice.</span><span class="sxs-lookup"><span data-stu-id="c6961-113">Sets or returns a **String** value, which is the name of the index.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6961-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6961-114">Remarks</span></span>

<span data-ttu-id="c6961-p101">O índice nomeado pela propriedade **Index** deve ter sido declarado anteriormente na tabela de base subjacente ao objeto **Recordset**. Ou seja, o índice deve ter sido declarado de forma programática como um objeto [Index](index-object-adox.md) do ADOX ou quando a tabela de base foi criada.</span><span class="sxs-lookup"><span data-stu-id="c6961-p101">The index named by the **Index** property must have previously been declared on the base table underlying the **Recordset** object. That is, the index must have been declared programmatically either as an ADOX [Index](index-object-adox.md) object, or when the base table was created.</span></span>

<span data-ttu-id="c6961-p102">Um erro de tempo de execução ocorrerá se o índice não puder ser definido. A propriedade **Index** não poderá ser definida:</span><span class="sxs-lookup"><span data-stu-id="c6961-p102">A run-time error will occur if the index cannot be set. The **Index** property cannot be set:</span></span>

  - <span data-ttu-id="c6961-119">Dentro de um manipulador de eventos [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) ou **RecordsetChangeComplete**.</span><span class="sxs-lookup"><span data-stu-id="c6961-119">Within a [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) or **RecordsetChangeComplete** event handler.</span></span>

  - <span data-ttu-id="c6961-120">Se o **Recordset** ainda estiver executando uma operação (o que pode ser determinado pela propriedade [State](state-property-ado.md)).</span><span class="sxs-lookup"><span data-stu-id="c6961-120">If the **Recordset** is still executing an operation (which can be determined by the [State](state-property-ado.md) property).</span></span>

  - <span data-ttu-id="c6961-121">Se um filtro tiver sido definido no **Recordset** com a propriedade [Filter](filter-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6961-121">If a filter has been set on the **Recordset** with the [Filter](filter-property-ado.md) property.</span></span>

<span data-ttu-id="c6961-122">A propriedade **Index** sempre poderá ser definida com sucesso se o **Recordset** estiver fechado, mas o **Recordset** não será aberto com sucesso, ou o índice não poderá ser usado, se o provedor de base não oferecer suporte a índices.</span><span class="sxs-lookup"><span data-stu-id="c6961-122">The **Index** property can always be set successfully if the **Recordset** is closed, but the **Recordset** will not open successfully, or the index will not be usable, if the underlying provider does not support indexes.</span></span>

<span data-ttu-id="c6961-p103">Se o índice puder ser definido, a posição da linha atual poderá ser alterada. Isso atualizará a propriedade [AbsolutePosition](absoluteposition-property-ado.md) e a geração dos eventos **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) e [MoveComplete](willmove-and-movecomplete-events-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6961-p103">If the index can be set, the current row position may change. This will cause an update to the [AbsolutePosition](absoluteposition-property-ado.md) property, and the generation of **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md), and [MoveComplete](willmove-and-movecomplete-events-ado.md) events.</span></span>

<span data-ttu-id="c6961-p104">Se o índice puder ser definido e a propriedade [LockType](locktype-property-ado.md) for **adLockPessimistic** ou **adLockOptimistic**, uma operação [UpdateBatch](updatebatch-method-ado.md) implícita será executada. Isso libera os grupos atuais e afetados. Qualquer filtro existente é liberado, e a posição da linha atual é alterada para a primeira linha do **Recordset** reordenado.</span><span class="sxs-lookup"><span data-stu-id="c6961-p104">If the index can be set and the [LockType](locktype-property-ado.md) property is **adLockPessimistic** or **adLockOptimistic**, then an implicit [UpdateBatch](updatebatch-method-ado.md) operation is performed. This releases the current and affected groups. Any existing filter is released, and the current row position is changed to the first row of the reordered **Recordset**.</span></span>

<span data-ttu-id="c6961-128">A propriedade **Index** é usada em conjunto com o método [Seek](seek-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6961-128">The **Index** property is used in conjunction with the [Seek](seek-method-ado.md) method.</span></span> <span data-ttu-id="c6961-129">Se o provedorde base não oferecer suporte à propriedade **Index** e, consequentemente, ao método **Seek**, considere o uso do método [Find](find-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6961-129">If the underlying provider does not support the **Index** property, and thus the **Seek** method, consider using the [Find](find-method-ado.md) method instead.</span></span> <span data-ttu-id="c6961-130">Determine se o objeto **Recordset** oferece suporte a índices com o método de **(adIndex)** [oferece suporte](supports-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c6961-130">Determine whether the **Recordset** object supports indexes with the [Supports](supports-method-ado.md)**(adIndex)** method.</span></span>

<span data-ttu-id="c6961-131">A propriedade interna **Index** não está relacionada à propriedade [Optimize](optimize-property-dynamic-ado.md) dinâmica, embora as duas lidem com índices.</span><span class="sxs-lookup"><span data-stu-id="c6961-131">The built-in **Index** property is not related to the dynamic [Optimize](optimize-property-dynamic-ado.md) property, although they both deal with indexes.</span></span>

