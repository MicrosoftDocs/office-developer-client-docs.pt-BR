---
<span data-ttu-id="106f2-101"><<<<<<< Título cabeça: propriedade PageCount (ADO) TOCTitle: propriedade PageCount (ADO) === título: propriedade PageCount (ADO) TOCTitle: propriedade PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="106f2-101"><<<<<<< HEAD title: PageCount Property (ADO) TOCTitle: PageCount Property (ADO) ======= title: PageCount property (ADO) TOCTitle: PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="106f2-102">ms:assetid de mestre: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: ms.date 48546609: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="106f2-102">master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="106f2-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="106f2-103"><<<<<<< HEAD</span></span>
# <a name="pagecount-property-ado"></a><span data-ttu-id="106f2-104">Propriedade PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="106f2-104">PageCount Property (ADO)</span></span>
=======
# <a name="pagecount-property-ado"></a><span data-ttu-id="106f2-105">Propriedade PageCount (ADO)</span><span class="sxs-lookup"><span data-stu-id="106f2-105">PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="106f2-106">mestre</span><span class="sxs-lookup"><span data-stu-id="106f2-106">master</span></span>


<span data-ttu-id="106f2-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="106f2-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="106f2-108">Indica a quantidade de páginas de dados que o objeto [Recordset](recordset-object-ado.md) contém.</span><span class="sxs-lookup"><span data-stu-id="106f2-108">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

<span data-ttu-id="106f2-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="106f2-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="106f2-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="106f2-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="106f2-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="106f2-111">Return value</span></span>
>>>>>>> <span data-ttu-id="106f2-112">mestre</span><span class="sxs-lookup"><span data-stu-id="106f2-112">master</span></span>

<span data-ttu-id="106f2-113">Retorna um valor **Long**, indicando a quantidade de páginas do **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="106f2-113">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="106f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="106f2-114">Remarks</span></span>

<span data-ttu-id="106f2-115">Utilize a propriedade **PageCount** para determinar a quantidade de páginas de dados contida no objeto **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="106f2-115">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="106f2-116">*Páginas* são grupos de registros cujo tamanho é igual a configuração da propriedade [PageSize](pagesize-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="106f2-116">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="106f2-117">Mesmo que a última página esteja incompleta por conter menos registros que no valor **PageSize**, ela será considerada como uma página adicional no valor **PageCount**.</span><span class="sxs-lookup"><span data-stu-id="106f2-117">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="106f2-118">Se o objeto **Recordset** não oferecer suporte a essa propriedade, o valor será -1, indicando que **PageCount** é indeterminável.</span><span class="sxs-lookup"><span data-stu-id="106f2-118">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="106f2-119">Consulte as propriedades **PageSize** e [AbsolutePage](absolutepage-property-ado.md) para obter mais informações sobre a funcionalidade da página.</span><span class="sxs-lookup"><span data-stu-id="106f2-119">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

