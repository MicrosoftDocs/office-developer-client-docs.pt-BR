---
<span data-ttu-id="0bb1f-101"><<<<<<< Título cabeça: propriedade Rowset (ADO) TOCTitle: propriedade Rowset (ADO) === título: propriedade Rowset (ADO) TOCTitle: propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="0bb1f-101"><<<<<<< HEAD title: Rowset Property (ADO) TOCTitle: Rowset Property (ADO) ======= title: Rowset property (ADO) TOCTitle: Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0bb1f-102">ms:assetid de mestre: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: ms.date 48543515: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0bb1f-102">master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0bb1f-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0bb1f-103"><<<<<<< HEAD</span></span>
# <a name="rowset-property-ado"></a><span data-ttu-id="0bb1f-104">Propriedade Rowset (ADO)</span><span class="sxs-lookup"><span data-stu-id="0bb1f-104">Rowset Property (ADO)</span></span>
=======
# <a name="rowset-property-ado"></a><span data-ttu-id="0bb1f-105">Propriedade RowSet (ADO)</span><span class="sxs-lookup"><span data-stu-id="0bb1f-105">Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0bb1f-106">mestre</span><span class="sxs-lookup"><span data-stu-id="0bb1f-106">master</span></span>


<span data-ttu-id="0bb1f-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0bb1f-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="0bb1f-108">Obtém ou define um objeto **Rowset** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-108">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="0bb1f-109">Quando você usa put\_Rowset, o conjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-109">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="0bb1f-110">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb1f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0bb1f-111">Syntax</span></span>

<span data-ttu-id="0bb1f-112">Get HRESULT\_Rowset (\[check-out, retval\] IUnknown\* \* ppRowset);</span><span class="sxs-lookup"><span data-stu-id="0bb1f-112">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="0bb1f-113">Colocar HRESULT\_Rowset (\[na\] IUnknown\* pRowset);</span><span class="sxs-lookup"><span data-stu-id="0bb1f-113">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="0bb1f-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bb1f-114">Parameters</span></span>

  - <span data-ttu-id="0bb1f-115">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="0bb1f-115">*ppRowset*</span></span>

  - <span data-ttu-id="0bb1f-116">Ponteiro para um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-116">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="0bb1f-117">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="0bb1f-117">*PRowset*</span></span>

  - <span data-ttu-id="0bb1f-118">Um objeto **Rowset** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-118">An OLE DB **Rowset** object.</span></span>

<span data-ttu-id="0bb1f-119"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="0bb1f-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="0bb1f-120">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="0bb1f-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="0bb1f-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0bb1f-121">Return values</span></span>
>>>>>>> <span data-ttu-id="0bb1f-122">mestre</span><span class="sxs-lookup"><span data-stu-id="0bb1f-122">master</span></span>

<span data-ttu-id="0bb1f-123">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="0bb1f-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="0bb1f-124">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="0bb1f-124">Applies To</span></span>

[<span data-ttu-id="0bb1f-125">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="0bb1f-125">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

