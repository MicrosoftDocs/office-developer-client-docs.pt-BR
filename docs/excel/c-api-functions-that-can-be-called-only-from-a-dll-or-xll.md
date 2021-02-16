---
title: Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api called from dll or xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423115"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="5b320-104">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="5b320-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="5b320-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5b320-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5b320-106">A API de C fornece 15 funções de retorno de chamada do Microsoft Excel que só podem ser chamadas usando as funções **Excel4**, **Excel4v**, **Excel12** ou **Excel12v** (ou por uma dessas funções indiretamente usando as funções de estrutura **Excel** ou **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="5b320-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="5b320-107">Isso significa que eles só podem ser chamados de uma DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="5b320-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="5b320-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5b320-108">In this section</span></span>

[<span data-ttu-id="5b320-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="5b320-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="5b320-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="5b320-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="5b320-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="5b320-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="5b320-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="5b320-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="5b320-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="5b320-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="5b320-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="5b320-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="5b320-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="5b320-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="5b320-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="5b320-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="5b320-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="5b320-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="5b320-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="5b320-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="5b320-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="5b320-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="5b320-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="5b320-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="5b320-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="5b320-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="5b320-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="5b320-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="5b320-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="5b320-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="5b320-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="5b320-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="5b320-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="5b320-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="5b320-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="5b320-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="5b320-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="5b320-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="5b320-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b320-128">See also</span></span>



[<span data-ttu-id="5b320-129">Retorno de chamada da API de C: funções Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="5b320-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

