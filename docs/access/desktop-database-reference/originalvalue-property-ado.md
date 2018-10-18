---
<span data-ttu-id="eac46-101"><<<<<<< Título cabeça: propriedade OriginalValue (ADO) TOCTitle: propriedade OriginalValue (ADO) === título: a propriedade OriginalValue (ADO) TOCTitle: a propriedade OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="eac46-101"><<<<<<< HEAD title: OriginalValue Property (ADO) TOCTitle: OriginalValue Property (ADO) ======= title: OriginalValue property (ADO) TOCTitle: OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="eac46-102">ms:assetid de mestre: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: ms.date 48542974: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="eac46-102">master ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="eac46-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="eac46-103"><<<<<<< HEAD</span></span>
# <a name="originalvalue-property-ado"></a><span data-ttu-id="eac46-104">Propriedade OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="eac46-104">OriginalValue Property (ADO)</span></span>
=======
# <a name="originalvalue-property-ado"></a><span data-ttu-id="eac46-105">Propriedade OriginalValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="eac46-105">OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="eac46-106">mestre</span><span class="sxs-lookup"><span data-stu-id="eac46-106">master</span></span>

<span data-ttu-id="eac46-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="eac46-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eac46-108">Indica o valor de um [Field](field-object-ado.md) que existia no registro antes de as alterações serem efetuadas.</span><span class="sxs-lookup"><span data-stu-id="eac46-108">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

<span data-ttu-id="eac46-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="eac46-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="eac46-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eac46-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="eac46-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eac46-111">Return value</span></span>
>>>>>>> <span data-ttu-id="eac46-112">mestre</span><span class="sxs-lookup"><span data-stu-id="eac46-112">master</span></span>

<span data-ttu-id="eac46-113">Retorna um valor **Variant** que representa o valor de um campo antes de qualquer alteração.</span><span class="sxs-lookup"><span data-stu-id="eac46-113">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="eac46-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eac46-114">Remarks</span></span>

<span data-ttu-id="eac46-115">Utilize a propriedade **OriginalValue** para retornar o valor do campo original de um campo a partir do registro atual.</span><span class="sxs-lookup"><span data-stu-id="eac46-115">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="eac46-116">No *modo de atualização imediata* (no qual o provedor grava as alterações à fonte de dados subjacente depois de chamar o método [Update](update-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que se encontrava antes que quaisquer alterações (ou seja, desde que o última chamada de método de **atualização** ).</span><span class="sxs-lookup"><span data-stu-id="eac46-116">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="eac46-117">Esse é o mesmo valor que o método [CancelUpdate](cancelupdate-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="eac46-117">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="eac46-118">No *modo de atualização em lotes* (no qual o provedor caches várias alterações e grava-los à fonte de dados subjacente somente quando você chamar o método [UpdateBatch](updatebatch-method-ado.md) ), a propriedade **OriginalValue** retorna o valor do campo que se encontrava antes de qualquer um altera (ou seja, desde o último método **UpdateBatch** é chamada).</span><span class="sxs-lookup"><span data-stu-id="eac46-118">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="eac46-119">Esse é o mesmo valor que o método [CancelBatch](cancelbatch-method-ado.md) utiliza para substituir a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="eac46-119">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="eac46-120">Quando você utiliza essa propriedade com a propriedade [UnderlyingValue](underlyingvalue-property-ado.md), é possível solucionar conflitos provenientes da atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="eac46-120">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="eac46-121">Registro</span><span class="sxs-lookup"><span data-stu-id="eac46-121">Record</span></span>

<span data-ttu-id="eac46-122">Para os objetos [Record](record-object-ado.md), a propriedade **OriginalValue** estará em branco nos campos adicionados antes da chamada do [ Update ](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="eac46-122">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

