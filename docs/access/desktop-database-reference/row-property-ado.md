---
<span data-ttu-id="28d39-101">título: propriedade Row - ActiveX Data Objects (ADO) <<<<<<< TOCTitle cabeça: propriedade de linha (ADO) === TOCTitle: linha de propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="28d39-101">title: Row Property - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Row Property (ADO) ======= TOCTitle: Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="28d39-102">ms:assetid de mestre: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: ms.date 48543562: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="28d39-102">master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="28d39-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="28d39-103"><<<<<<< HEAD</span></span>
# <a name="row-property-ado"></a><span data-ttu-id="28d39-104">Propriedade Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="28d39-104">Row Property (ADO)</span></span>
=======
# <a name="row-property-ado"></a><span data-ttu-id="28d39-105">Propriedade Row (ADO)</span><span class="sxs-lookup"><span data-stu-id="28d39-105">Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="28d39-106">mestre</span><span class="sxs-lookup"><span data-stu-id="28d39-106">master</span></span>


<span data-ttu-id="28d39-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="28d39-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="28d39-108">Obtém ou define um objeto **Row** do OLE DB a partir de/em um objeto **ADORecordConstruction**.</span><span class="sxs-lookup"><span data-stu-id="28d39-108">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="28d39-109">Quando você usa **colocar\_linha** para definir um objeto **Row** , uma linha seja transformada em um objeto **Record** do ADO.</span><span class="sxs-lookup"><span data-stu-id="28d39-109">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="28d39-110">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="28d39-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d39-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="28d39-111">Syntax</span></span>

<span data-ttu-id="28d39-112">Get HRESULT\_linha (\[check-out, retval\] IUnknown\* \* ppRow);</span><span class="sxs-lookup"><span data-stu-id="28d39-112">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="28d39-113">Colocar HRESULT\_linha (\[na\] IUnknown\* pRow);</span><span class="sxs-lookup"><span data-stu-id="28d39-113">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="28d39-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="28d39-114">Parameters</span></span>

  - <span data-ttu-id="28d39-115">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="28d39-115">*ppRow*</span></span>

  - <span data-ttu-id="28d39-116">Ponteiro para um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="28d39-116">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="28d39-117">*PRow*</span><span class="sxs-lookup"><span data-stu-id="28d39-117">*PRow*</span></span>

  - <span data-ttu-id="28d39-118">Um objeto **Row** do OLE DB.</span><span class="sxs-lookup"><span data-stu-id="28d39-118">An OLE DB **Row** object.</span></span>

<span data-ttu-id="28d39-119"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="28d39-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="28d39-120">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="28d39-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="28d39-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="28d39-121">Return values</span></span>
>>>>>>> <span data-ttu-id="28d39-122">mestre</span><span class="sxs-lookup"><span data-stu-id="28d39-122">master</span></span>

<span data-ttu-id="28d39-123">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="28d39-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="28d39-124">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="28d39-124">Applies To</span></span>

[<span data-ttu-id="28d39-125">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="28d39-125">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

