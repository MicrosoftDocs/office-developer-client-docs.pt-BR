---
<span data-ttu-id="ac7eb-101"><<<<<<< Título cabeça: propriedade Precision (ADO) TOCTitle: propriedade Precision (ADO) === título: propriedade Precision (ADO) TOCTitle: a propriedade Precision (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-101"><<<<<<< HEAD title: Precision Property (ADO) TOCTitle: Precision Property (ADO) ======= title: Precision property (ADO) TOCTitle: Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ac7eb-102">ms:assetid de mestre: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: ms.date 48547685: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ac7eb-102">master ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="ac7eb-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ac7eb-103"><<<<<<< HEAD</span></span>
# <a name="precision-property-ado"></a><span data-ttu-id="ac7eb-104">Propriedade Precision (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-104">Precision Property (ADO)</span></span>
=======
# <a name="precision-property-ado"></a><span data-ttu-id="ac7eb-105">Propriedade Precision (ADO)</span><span class="sxs-lookup"><span data-stu-id="ac7eb-105">Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ac7eb-106">mestre</span><span class="sxs-lookup"><span data-stu-id="ac7eb-106">master</span></span>


<span data-ttu-id="ac7eb-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac7eb-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac7eb-108">Indica o grau de precisão de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou de objetos [Field](field-object-ado.md) numéricos.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-108">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

<span data-ttu-id="ac7eb-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ac7eb-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ac7eb-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ac7eb-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ac7eb-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ac7eb-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ac7eb-112">mestre</span><span class="sxs-lookup"><span data-stu-id="ac7eb-112">master</span></span>

<span data-ttu-id="ac7eb-113">Define ou retorna um valor **Byte** que indica o número máximo de dígitos utilizado para representar os valores.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-113">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac7eb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac7eb-114">Remarks</span></span>

<span data-ttu-id="ac7eb-115">Utilize a propriedade **Precision** para determinar o número máximo de dígitos utilizado para representar os valores de um objeto numérico **Parameter** ou **Field**.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-115">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="ac7eb-116">O valor é leitura/gravação em um objeto **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-116">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="ac7eb-p101">Para um objeto **Field**, a propriedade **Precision** normalmente é somente leitura. Entretanto, para novos objetos **Field** que tenham sido acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Precision** será leitura/gravação somente depois que a propriedade [Value](value-property-ado.md) de **Field** tiver sido especificada e o provedor de dados tiver adicionado com êxito o novo **Field** por meio da chamada do método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="ac7eb-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

