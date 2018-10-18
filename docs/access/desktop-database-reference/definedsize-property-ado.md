---
<span data-ttu-id="0dcac-101"><<<<<<< Título cabeça: propriedade DefinedSize (ADO) TOCTitle: propriedade DefinedSize (ADO) === título: propriedade DefinedSize (ADO) TOCTitle: a propriedade DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dcac-101"><<<<<<< HEAD title: DefinedSize Property (ADO) TOCTitle: DefinedSize Property (ADO) ======= title: DefinedSize property (ADO) TOCTitle: DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0dcac-102">ms:assetid de mestre: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: ms.date 48546257: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0dcac-102">master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0dcac-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0dcac-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-ado"></a><span data-ttu-id="0dcac-104">Propriedade DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dcac-104">DefinedSize Property (ADO)</span></span>
=======
# <a name="definedsize-property-ado"></a><span data-ttu-id="0dcac-105">Propriedade DefinedSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="0dcac-105">DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0dcac-106">mestre</span><span class="sxs-lookup"><span data-stu-id="0dcac-106">master</span></span>


<span data-ttu-id="0dcac-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0dcac-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0dcac-108">Indica a capacidade de dados de um objeto [Field](field-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="0dcac-108">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="0dcac-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0dcac-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0dcac-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0dcac-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0dcac-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0dcac-111">Return value</span></span>
>>>>>>> <span data-ttu-id="0dcac-112">mestre</span><span class="sxs-lookup"><span data-stu-id="0dcac-112">master</span></span>

<span data-ttu-id="0dcac-113">Retorna um valor **Long** que reflete o tamanho definido de um campo como um número de bytes.</span><span class="sxs-lookup"><span data-stu-id="0dcac-113">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dcac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0dcac-114">Remarks</span></span>

<span data-ttu-id="0dcac-115">Use a propriedade **DefinedSize** para determinar a capacidade de dados de um objeto **Field**.</span><span class="sxs-lookup"><span data-stu-id="0dcac-115">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="0dcac-p101">As propriedades **DefinedSize** e [ActualSize](actualsize-property-ado.md) são diferentes. Por exemplo, considere um objeto **Field** com um tipo declarado de **adVarChar** e um valor de propriedade **DefinedSize** de 50, contendo um único caractere. O valor da propriedade **ActualSize** retornado será a extensão em bytes deste único caractere.</span><span class="sxs-lookup"><span data-stu-id="0dcac-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

