---
title: Novidades na API de C para Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007], novidades
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439685"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="f3b78-104">Novidades na API de C para Excel</span><span class="sxs-lookup"><span data-stu-id="f3b78-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="f3b78-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f3b78-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f3b78-106">Em conjunto com o Microsoft Excel 2013, o Microsoft Excel 2013 XLL Software Development Kit (SDK) inclui suporte para os seguintes recursos.</span><span class="sxs-lookup"><span data-stu-id="f3b78-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="f3b78-107">**Novas funções**</span><span class="sxs-lookup"><span data-stu-id="f3b78-107">**New Functions**</span></span>
    
    <span data-ttu-id="f3b78-108">O Microsoft Excel 2013 XLL SDK dá suporte à chamada de volta para todas as novas funções de planilha no Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="f3b78-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="f3b78-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="f3b78-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="f3b78-110">**Funções assíncronas definidas pelo usuário**</span><span class="sxs-lookup"><span data-stu-id="f3b78-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="f3b78-111">O Excel 2013 dá suporte à chamada assíncrona de funções definidas pelo usuário (UDF), o que pode melhorar o desempenho habilitando vários cálculos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="f3b78-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="f3b78-112">Para obter mais informações sobre UDFs assíncronas, consulte Funções de User-Defined [assíncronas.](asynchronous-user-defined-functions.md)</span><span class="sxs-lookup"><span data-stu-id="f3b78-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="f3b78-113">**Conectores de cluster**</span><span class="sxs-lookup"><span data-stu-id="f3b78-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="f3b78-114">Os conectores de cluster permitem que as UDFs executem em clusters de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="f3b78-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="f3b78-115">Para obter mais informações sobre como criar conectores de cluster, consulte [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="f3b78-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f3b78-116">Os complementos XLL que você pretende executar em clusters de computação devem chamar apenas funções seguras para cluster.</span><span class="sxs-lookup"><span data-stu-id="f3b78-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="f3b78-117">Para obter mais informações sobre as funções que você pode usar, consulte Excel [XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f3b78-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="f3b78-118">**Suporte de 64 bits**</span><span class="sxs-lookup"><span data-stu-id="f3b78-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="f3b78-119">Agora você pode compilar e vincular XLLs de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f3b78-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="f3b78-120">Para obter mais informações, consulte [Criando XLLs](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="f3b78-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f3b78-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="f3b78-121">See also</span></span>



[<span data-ttu-id="f3b78-122">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="f3b78-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="f3b78-123">Programação com a API de C no Excel</span><span class="sxs-lookup"><span data-stu-id="f3b78-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="f3b78-124">Contenção de memória e multithreading no Excel</span><span class="sxs-lookup"><span data-stu-id="f3b78-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="f3b78-125">Introdução ao Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="f3b78-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

