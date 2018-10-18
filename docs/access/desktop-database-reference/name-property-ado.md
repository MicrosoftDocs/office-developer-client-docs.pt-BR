---
<span data-ttu-id="34b97-101"><<<<<<< Título cabeça: TOCTitle nome Property (ADO): nome Property (ADO) === título: nome de propriedade (ADO) TOCTitle: nome de propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="34b97-101"><<<<<<< HEAD title: Name Property (ADO) TOCTitle: Name Property (ADO) ======= title: Name property (ADO) TOCTitle: Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="34b97-102">ms:assetid de mestre: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: ms.date 48544683: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="34b97-102">master ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15) ms:contentKeyID: 48544683 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="34b97-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="34b97-103"><<<<<<< HEAD</span></span>
# <a name="name-property-ado"></a><span data-ttu-id="34b97-104">Propriedade Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="34b97-104">Name Property (ADO)</span></span>
=======
# <a name="name-property-ado"></a><span data-ttu-id="34b97-105">Propriedade Name (ADO)</span><span class="sxs-lookup"><span data-stu-id="34b97-105">Name property (ADO)</span></span>
>>>>>>> <span data-ttu-id="34b97-106">mestre</span><span class="sxs-lookup"><span data-stu-id="34b97-106">master</span></span>


<span data-ttu-id="34b97-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="34b97-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="34b97-108">Indica o nome de um objeto</span><span class="sxs-lookup"><span data-stu-id="34b97-108">Indicates the name of an object.</span></span>

<span data-ttu-id="34b97-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="34b97-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="34b97-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="34b97-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="34b97-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="34b97-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="34b97-112">mestre</span><span class="sxs-lookup"><span data-stu-id="34b97-112">master</span></span>

<span data-ttu-id="34b97-113">Define ou retorna um valor **String** que indica o nome de um objeto.</span><span class="sxs-lookup"><span data-stu-id="34b97-113">Sets or returns a **String** value that indicates the name of an object.</span></span>

## <a name="remarks"></a><span data-ttu-id="34b97-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="34b97-114">Remarks</span></span>

<span data-ttu-id="34b97-115">Use a propriedade **Name** para atribuir um nome ou recuperar o nome de um objeto **Command**, **Property**, **Field** ou **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="34b97-115">Use the **Name** property to assign a name to or retrieve the name of a **Command**, **Property**, **Field**, or **Parameter** object.</span></span>

<span data-ttu-id="34b97-116">O valor é leitura/gravação em um objeto **Command** e somente leitura em um objeto **Property**.</span><span class="sxs-lookup"><span data-stu-id="34b97-116">The value is read/write on a **Command** object and read-only on a **Property** object.</span></span>

<span data-ttu-id="34b97-p101">Para um objeto **Field**, **Name** normalmente é somente leitura. No entanto, para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um [Record](record-object-ado.md), **Name** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para **Field** for especificada e o provedor de dados adicionar com sucesso o novo **Field** chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="34b97-p101">For a **Field** object, **Name** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Name** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="34b97-p102">Para os objetos **Parameter** que ainda não foram acrescentados à coleção [Parameters](parameters-collection-ado.md), a propriedade **Name** é leitura/gravação. Para objetos **Parameter** acrescentados e todos os outros objetos, a propriedade **Name** é somente leitura. Os nomes não precisam ser exclusivos em uma coleção.</span><span class="sxs-lookup"><span data-stu-id="34b97-p102">For **Parameter** objects not yet appended to the [Parameters](parameters-collection-ado.md) collection, the **Name** property is read/write. For appended **Parameter** objects and all other objects, the **Name** property is read-only. Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="34b97-122">Você pode recuperar a propriedade **Name** de um objeto por uma referência ordinal, após a qual pode se referir ao objeto diretamente pelo nome.</span><span class="sxs-lookup"><span data-stu-id="34b97-122">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name.</span></span> <span data-ttu-id="34b97-123">Por exemplo, se rstMain.Properties(20). Nome produz a capacidade de atualização, você pode se referir a essa propriedade como produz a capacidade de atualização, você pode se referir a essa propriedade como rstMain.Properties("Updatability").</span><span class="sxs-lookup"><span data-stu-id="34b97-123">For example, if rstMain.Properties(20).Name yields Updatability , you can subsequently refer to this property as yields Updatability , you can subsequently refer to this property as rstMain.Properties("Updatability") .</span></span>

