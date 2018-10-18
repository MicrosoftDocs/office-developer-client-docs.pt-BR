---
<span data-ttu-id="74f2a-101"><<<<<<< Título cabeça: propriedade NumericScale (ADO) TOCTitle: propriedade NumericScale (ADO) === título: a propriedade NumericScale (ADO) TOCTitle: a propriedade NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="74f2a-101"><<<<<<< HEAD title: NumericScale Property (ADO) TOCTitle: NumericScale Property (ADO) ======= title: NumericScale property (ADO) TOCTitle: NumericScale property (ADO)</span></span>
>>>>>>> <span data-ttu-id="74f2a-102">ms:assetid de mestre: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: ms.date 48544824: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="74f2a-102">master ms:assetid: 51b232d2-5bfd-521c-f4e9-65655ecc7c70 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249263(v=office.15) ms:contentKeyID: 48544824 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="74f2a-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="74f2a-103"><<<<<<< HEAD</span></span>
# <a name="numericscale-property-ado"></a><span data-ttu-id="74f2a-104">Propriedade NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="74f2a-104">NumericScale Property (ADO)</span></span>
=======
# <a name="numericscale-property-ado"></a><span data-ttu-id="74f2a-105">Propriedade NumericScale (ADO)</span><span class="sxs-lookup"><span data-stu-id="74f2a-105">NumericScale property (ADO)</span></span>
>>>>>>> <span data-ttu-id="74f2a-106">mestre</span><span class="sxs-lookup"><span data-stu-id="74f2a-106">master</span></span>


<span data-ttu-id="74f2a-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="74f2a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="74f2a-108">Indica a escala de valores numéricos em um objeto [Parameter](parameter-object-ado.md) ou [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="74f2a-108">Indicates the scale of numeric values in a [Parameter](parameter-object-ado.md) or [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="74f2a-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="74f2a-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="74f2a-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="74f2a-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="74f2a-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="74f2a-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="74f2a-112">mestre</span><span class="sxs-lookup"><span data-stu-id="74f2a-112">master</span></span>

<span data-ttu-id="74f2a-113">Define ou retorna um valor **Byte** que indica o número de casas decimais para as quais os valores numéricos serão resolvidos.</span><span class="sxs-lookup"><span data-stu-id="74f2a-113">Sets or returns a **Byte** value that indicates the number of decimal places to which numeric values will be resolved.</span></span>

## <a name="remarks"></a><span data-ttu-id="74f2a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="74f2a-114">Remarks</span></span>

<span data-ttu-id="74f2a-115">Use a propriedade **NumericScale** para determinar quantos dígitos à direita da vírgula decimal serão usados para representar valores de um objeto numérico **Parameter** ou **Field**.</span><span class="sxs-lookup"><span data-stu-id="74f2a-115">Use the **NumericScale** property to determine how many digits to the right of the decimal point will be used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="74f2a-116">Em objetos **Parameter**, a propriedade **NumericScale** é leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="74f2a-116">For **Parameter** objects, the **NumericScale** property is read/write.</span></span>

<span data-ttu-id="74f2a-p101">Em um objeto **Field**, **NumericScale** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **NumericScale** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** for especificada e o provedor de dados tiver adicionado com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="74f2a-p101">For a **Field** object, **NumericScale** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **NumericScale** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

