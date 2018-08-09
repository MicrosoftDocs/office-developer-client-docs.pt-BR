---
title: Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [excel 2007], api c chamada de dll ou xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765266"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="f2063-104">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="f2063-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="f2063-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f2063-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f2063-106">A API C fornece funções de retorno de chamada do Microsoft Excel 15 que só podem ser chamadas usando o **Excel4**, **Excel4v**, **Excel12**ou funções **Excel12v** (ou uma dessas funções indiretamente usando as funções de Framework **Excel **ou **Excel12f**).</span><span class="sxs-lookup"><span data-stu-id="f2063-106">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**).</span></span> <span data-ttu-id="f2063-107">Isso significa que só pode ser chamados por um DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="f2063-107">This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="f2063-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f2063-108">In this section</span></span>

[<span data-ttu-id="f2063-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="f2063-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="f2063-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="f2063-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="f2063-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="f2063-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="f2063-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="f2063-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="f2063-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="f2063-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="f2063-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="f2063-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="f2063-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="f2063-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="f2063-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="f2063-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="f2063-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="f2063-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="f2063-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="f2063-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="f2063-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="f2063-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="f2063-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="f2063-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="f2063-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="f2063-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="f2063-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="f2063-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="f2063-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="f2063-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="f2063-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="f2063-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="f2063-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="f2063-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="f2063-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="f2063-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="f2063-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="f2063-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="f2063-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2063-128">See also</span></span>



[<span data-ttu-id="f2063-129">C API Callback Functions Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="f2063-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

