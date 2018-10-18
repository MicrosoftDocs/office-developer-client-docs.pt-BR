---
<span data-ttu-id="24f80-101"><<<<<<< Título cabeça: TOCTitle capítulo Property (ADO): capítulo Property (ADO) === título: propriedade Chapter (ADO) TOCTitle: propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="24f80-101"><<<<<<< HEAD title: Chapter Property (ADO) TOCTitle: Chapter Property (ADO) ======= title: Chapter property (ADO) TOCTitle: Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="24f80-102">ms:assetid de mestre: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: ms.date 48548014: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="24f80-102">master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="24f80-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="24f80-103"><<<<<<< HEAD</span></span>
# <a name="chapter-property-ado"></a><span data-ttu-id="24f80-104">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="24f80-104">Chapter Property (ADO)</span></span>
=======
# <a name="chapter-property-ado"></a><span data-ttu-id="24f80-105">Propriedade Chapter (ADO)</span><span class="sxs-lookup"><span data-stu-id="24f80-105">Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="24f80-106">mestre</span><span class="sxs-lookup"><span data-stu-id="24f80-106">master</span></span>


<span data-ttu-id="24f80-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="24f80-107">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="24f80-108">Obtém ou configura um objeto **Chapter** do OLE DB de/em um objeto **ADORecordsetConstruction**.</span><span class="sxs-lookup"><span data-stu-id="24f80-108">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="24f80-109">Quando você usa **colocar\_capítulo** para definir o objeto de **capítulo** , um subconjunto de linhas seja transformado em um objeto **Recordset** do ADO.</span><span class="sxs-lookup"><span data-stu-id="24f80-109">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="24f80-110">Isso define o capítulo atual do objeto **Rowset**.</span><span class="sxs-lookup"><span data-stu-id="24f80-110">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="24f80-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="24f80-111">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="24f80-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24f80-112">Syntax</span></span>

<span data-ttu-id="24f80-113">Get HRESULT\_capítulo (\[check-out, retval\] longo\* plChapter);</span><span class="sxs-lookup"><span data-stu-id="24f80-113">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="24f80-114">Colocar HRESULT\_capítulo (\[na\] lChapter longo);</span><span class="sxs-lookup"><span data-stu-id="24f80-114">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="24f80-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24f80-115">Parameters</span></span>

  - <span data-ttu-id="24f80-116">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="24f80-116">*plChapter*</span></span>

  - <span data-ttu-id="24f80-117">Ponteiro para o identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="24f80-117">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="24f80-118">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="24f80-118">*LChapter*</span></span>

  - <span data-ttu-id="24f80-119">Identificador de um capítulo.</span><span class="sxs-lookup"><span data-stu-id="24f80-119">Handle of a chapter.</span></span>

<span data-ttu-id="24f80-120"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="24f80-120"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="24f80-121">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="24f80-121">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="24f80-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="24f80-122">Return values</span></span>
>>>>>>> <span data-ttu-id="24f80-123">mestre</span><span class="sxs-lookup"><span data-stu-id="24f80-123">master</span></span>

<span data-ttu-id="24f80-124">Esse método de propriedade retorna os valores padrão HRESULT, incluindo S\_Okey e f\_falhar.</span><span class="sxs-lookup"><span data-stu-id="24f80-124">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="24f80-125">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="24f80-125">Applies To</span></span>

[<span data-ttu-id="24f80-126">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="24f80-126">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

