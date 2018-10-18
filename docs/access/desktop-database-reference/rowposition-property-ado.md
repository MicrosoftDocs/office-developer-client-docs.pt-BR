---
<span data-ttu-id="c9282-101"><<<<<<< Título cabeça: propriedade RowPosition (ADO) TOCTitle: propriedade RowPosition (ADO) === título: propriedade RowPosition (ADO) TOCTitle: propriedade RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9282-101"><<<<<<< HEAD title: RowPosition Property (ADO) TOCTitle: RowPosition Property (ADO) ======= title: RowPosition property (ADO) TOCTitle: RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c9282-102">ms:assetid de mestre: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: ms.date 48547325: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="c9282-102">master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="c9282-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9282-103"><<<<<<< HEAD</span></span>
# <a name="rowposition-property-ado"></a><span data-ttu-id="c9282-104">Propriedade RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9282-104">RowPosition Property (ADO)</span></span>
=======
# <a name="rowposition-property-ado"></a><span data-ttu-id="c9282-105">Propriedade RowPosition (ADO)</span><span class="sxs-lookup"><span data-stu-id="c9282-105">RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c9282-106">mestre</span><span class="sxs-lookup"><span data-stu-id="c9282-106">master</span></span>


<span data-ttu-id="c9282-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9282-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="c9282-108">Obtém ou define um objeto **RowPosition** do OLE DB a partir de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="c9282-108">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="c9282-109">Quando você usa **colocar\_RowPosition** para definir o objeto **RowPosition** , o objeto **Recordset** resultante usa o objeto **RowPosition** para determinar a linha atual.</span><span class="sxs-lookup"><span data-stu-id="c9282-109">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="c9282-110">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c9282-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9282-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9282-111">Syntax</span></span>

<span data-ttu-id="c9282-112">Get HRESULT\_RowPosition (\[check-out, retval\] IUnknown\* \* ppRowPos);</span><span class="sxs-lookup"><span data-stu-id="c9282-112">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="c9282-113">Colocar HRESULT\_RowPosition (\[na\] IUnknown\* pRowPos);</span><span class="sxs-lookup"><span data-stu-id="c9282-113">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="c9282-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9282-114">Parameters</span></span>

  - <span data-ttu-id="c9282-115">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="c9282-115">*ppRowPos*</span></span>

  - <span data-ttu-id="c9282-116">Ponteiro para um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9282-116">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="c9282-117">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="c9282-117">*PRowPos*</span></span>

  - <span data-ttu-id="c9282-118">Um objeto **RowPosition** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="c9282-118">An OLE DB **RowPosition** object.</span></span>

<span data-ttu-id="c9282-119"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="c9282-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="c9282-120">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="c9282-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="c9282-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c9282-121">Return values</span></span>
>>>>>>> <span data-ttu-id="c9282-122">mestre</span><span class="sxs-lookup"><span data-stu-id="c9282-122">master</span></span>

<span data-ttu-id="c9282-123">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="c9282-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9282-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9282-124">Remarks</span></span>

<span data-ttu-id="c9282-p102">Quando esta propriedade for definida, se o objeto **Rowset** no objeto **RowPosition** for diferente do objeto **Rowset** no objeto **Recordset**, o primeiro substituirá o segundo. O mesmo comportamento também se aplicará ao **Charter** atual do **RowPosition**.</span><span class="sxs-lookup"><span data-stu-id="c9282-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c9282-127">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c9282-127">Applies To</span></span>

[<span data-ttu-id="c9282-128">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="c9282-128">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

