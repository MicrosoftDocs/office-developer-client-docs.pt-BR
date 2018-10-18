---
<span data-ttu-id="6e361-101"><<<<<<< Título cabeça: propriedade PageSize (ADO) TOCTitle: propriedade PageSize (ADO) === título: propriedade PageSize (ADO) TOCTitle: propriedade PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="6e361-101"><<<<<<< HEAD title: PageSize Property (ADO) TOCTitle: PageSize Property (ADO) ======= title: PageSize property (ADO) TOCTitle: PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6e361-102">ms:assetid de mestre: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: ms.date 48548079: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="6e361-102">master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="6e361-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="6e361-103"><<<<<<< HEAD</span></span>
# <a name="pagesize-property-ado"></a><span data-ttu-id="6e361-104">Propriedade PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="6e361-104">PageSize Property (ADO)</span></span>
=======
# <a name="pagesize-property-ado"></a><span data-ttu-id="6e361-105">Propriedade PageSize (ADO)</span><span class="sxs-lookup"><span data-stu-id="6e361-105">PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="6e361-106">mestre</span><span class="sxs-lookup"><span data-stu-id="6e361-106">master</span></span>


<span data-ttu-id="6e361-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e361-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6e361-108">Indica quantos registros formam uma página no [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="6e361-108">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="6e361-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="6e361-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="6e361-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6e361-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="6e361-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6e361-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="6e361-112">mestre</span><span class="sxs-lookup"><span data-stu-id="6e361-112">master</span></span>

<span data-ttu-id="6e361-p101">Define ou retorna um valor **Long** que indica quantos registros estão presentes em uma página. O padrão é 10.</span><span class="sxs-lookup"><span data-stu-id="6e361-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e361-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e361-115">Remarks</span></span>

<span data-ttu-id="6e361-116"><<<<<<< Cabeça Use a propriedade **PageSize** para determinar quantos registros formam uma página lógica dos dados.</span><span class="sxs-lookup"><span data-stu-id="6e361-116"><<<<<<< HEAD Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="6e361-117">Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="6e361-117">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="6e361-118">Isso é útil em cenários de servidores Web quando se deseja permitir que o usuário pagine os dados, exibindo um certo número de registros ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6e361-118">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
<span data-ttu-id="6e361-119">=== Use a propriedade **PageSize** para determinar quantos registros formam uma página lógica dos dados.</span><span class="sxs-lookup"><span data-stu-id="6e361-119">======= Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="6e361-120">Estabelecer um tamanho de página permite que você use a propriedade [AbsolutePage](absolutepage-property-ado.md) para mover-se até o primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="6e361-120">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="6e361-121">Isso é útil em cenários de servidor da web quando você deseja permitir que o usuário à página através de dados, exibindo um determinado número de registros por vez.</span><span class="sxs-lookup"><span data-stu-id="6e361-121">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
>>>>>>> <span data-ttu-id="6e361-122">mestre</span><span class="sxs-lookup"><span data-stu-id="6e361-122">master</span></span>

<span data-ttu-id="6e361-123">Essa propriedade pode ser definida a qualquer momento e seu valor será utilizado para calcular o local do primeiro registro de uma página específica.</span><span class="sxs-lookup"><span data-stu-id="6e361-123">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

