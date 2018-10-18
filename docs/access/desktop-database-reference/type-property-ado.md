---
<span data-ttu-id="c79eb-101"><<<<<<< Título cabeça: TOCTitle propriedade tipo (ADO): tipo de propriedade (ADO) === título: (ADO) a propriedade Type TOCTitle: digite propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="c79eb-101"><<<<<<< HEAD title: Type Property (ADO) TOCTitle: Type Property (ADO) ======= title: Type property (ADO) TOCTitle: Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c79eb-102">ms:assetid de mestre: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: ms.date 48543397: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c79eb-102">master ms:assetid: 14d99172-2145-05ae-620b-459ba097f05c ms:mtpsurl: https://msdn.microsoft.com/library/JJ248914(v=office.15) ms:contentKeyID: 48543397 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c79eb-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c79eb-103"><<<<<<< HEAD</span></span>
# <a name="type-property-ado"></a><span data-ttu-id="c79eb-104">Propriedade Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="c79eb-104">Type Property (ADO)</span></span>
=======
# <a name="type-property-ado"></a><span data-ttu-id="c79eb-105">Propriedade Type (ADO)</span><span class="sxs-lookup"><span data-stu-id="c79eb-105">Type property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c79eb-106">mestre</span><span class="sxs-lookup"><span data-stu-id="c79eb-106">master</span></span>


<span data-ttu-id="c79eb-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c79eb-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c79eb-108">Indica o tipo operacional ou o tipo de dados de um objeto [Parameter](parameter-object-ado.md), [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c79eb-108">Indicates the operational type or data type of a [Parameter](parameter-object-ado.md), [Field](field-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="c79eb-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c79eb-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="c79eb-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c79eb-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="c79eb-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c79eb-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="c79eb-112">mestre</span><span class="sxs-lookup"><span data-stu-id="c79eb-112">master</span></span>

<span data-ttu-id="c79eb-113">Define ou retorna um valor [DataTypeEnum](datatypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="c79eb-113">Sets or returns a [DataTypeEnum](datatypeenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c79eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c79eb-114">Remarks</span></span>

<span data-ttu-id="c79eb-p101">Para os objetos **Parameter**, a propriedade **Type** é leitura/gravação. Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Type** é leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados adicionar com êxito o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="c79eb-p101">For **Parameter** objects, the **Type** property is read/write. For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Type** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="c79eb-117">Para todos os outros objetos, a propriedade **Type** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="c79eb-117">For all other objects, the **Type** property is read-only.</span></span>

