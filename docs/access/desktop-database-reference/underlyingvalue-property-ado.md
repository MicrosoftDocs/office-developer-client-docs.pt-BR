---
<span data-ttu-id="ceaaf-101"><<<<<<< Título cabeça: propriedade UnderlyingValue (ADO) TOCTitle: propriedade UnderlyingValue (ADO) === título: propriedade UnderlyingValue (ADO) TOCTitle: propriedade UnderlyingValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="ceaaf-101"><<<<<<< HEAD title: UnderlyingValue Property (ADO) TOCTitle: UnderlyingValue Property (ADO) ======= title: UnderlyingValue property (ADO) TOCTitle: UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ceaaf-102">ms:assetid de mestre: f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID: ms.date 48548782: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ceaaf-102">master ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID: 48548782 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ceaaf-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ceaaf-103"><<<<<<< HEAD</span></span>
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="ceaaf-104">Propriedade UnderlyingValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="ceaaf-104">UnderlyingValue Property (ADO)</span></span>
=======
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="ceaaf-105">Propriedade UnderlyingValue (ADO)</span><span class="sxs-lookup"><span data-stu-id="ceaaf-105">UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ceaaf-106">mestre</span><span class="sxs-lookup"><span data-stu-id="ceaaf-106">master</span></span>


<span data-ttu-id="ceaaf-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ceaaf-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="ceaaf-108">Indica um valor atual do objeto [Field](field-object-ado.md) no banco de dados.</span><span class="sxs-lookup"><span data-stu-id="ceaaf-108">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

<span data-ttu-id="ceaaf-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ceaaf-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="ceaaf-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ceaaf-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="ceaaf-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ceaaf-111">Return value</span></span>
>>>>>>> <span data-ttu-id="ceaaf-112">mestre</span><span class="sxs-lookup"><span data-stu-id="ceaaf-112">master</span></span>

<span data-ttu-id="ceaaf-113">Retorna um valor **Variant** que indica o valor do **Field**.</span><span class="sxs-lookup"><span data-stu-id="ceaaf-113">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceaaf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ceaaf-114">Remarks</span></span>

<span data-ttu-id="ceaaf-p101">Utilize a propriedade **UnderlyingValue** para retornar o valor de campo atual do banco de dados. O valor de campo na propriedade **UnderlyingValue** é o valor visível para sua transação e pode ser o resultado de uma atualização recente efetuada por outra transação. Ele pode ser diferente da propriedade [OriginalValue](originalvalue-property-ado.md), que reflete o valor que foi retornado originalmente para o [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ceaaf-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="ceaaf-p102">Isto é semelhante ao uso do método [Resync](resync-method-ado.md), mas a propriedade **UnderlyingValue** retorna somente o valor para um campo específico do registro atual. Esse é o mesmo valor que o método [Resync](resync-method-ado.md) utiliza para substituir a propriedade [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ceaaf-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="ceaaf-120">Quando você utiliza essa propriedade com a propriedade **OriginalValue**, é possível solucionar conflitos provenientes de atualizações em lote.</span><span class="sxs-lookup"><span data-stu-id="ceaaf-120">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="ceaaf-121">Registro</span><span class="sxs-lookup"><span data-stu-id="ceaaf-121">Record</span></span>

<span data-ttu-id="ceaaf-122">Nos objetos [Record](record-object-ado.md), esta propriedade estará vazia para os campos adicionados antes de o [Update](update-method-ado.md) ser chamado.</span><span class="sxs-lookup"><span data-stu-id="ceaaf-122">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

