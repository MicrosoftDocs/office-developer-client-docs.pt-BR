---
title: Novidades na API de C do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- a api c [excel 2007], o que há de novo
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19765440"
---
# <a name="whats-new-in-the-c-api-for-excel"></a><span data-ttu-id="cb175-104">Novidades na API de C do Excel</span><span class="sxs-lookup"><span data-stu-id="cb175-104">What's New in the C API for Excel</span></span>

 <span data-ttu-id="cb175-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cb175-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cb175-106">Em conjunto com o Microsoft Excel 2013, o Microsoft Excel 2013 XLL Software Development Kit (SDK) inclui o suporte para os recursos a seguintes.</span><span class="sxs-lookup"><span data-stu-id="cb175-106">In conjunction with Microsoft Excel 2013, the Microsoft Excel 2013 XLL Software Development Kit (SDK) includes support for the following features.</span></span>
  
- <span data-ttu-id="cb175-107">**Novas funções**</span><span class="sxs-lookup"><span data-stu-id="cb175-107">**New Functions**</span></span>
    
    <span data-ttu-id="cb175-108">O Microsoft Excel 2013 XLL SDK suporta chamar de volta todas as novas funções de planilha no Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="cb175-108">The Microsoft Excel 2013 XLL SDK supports calling back to all of the new worksheet functions in Excel 2013.</span></span> <span data-ttu-id="cb175-109">Para obter mais informações sobre como chamar funções do Excel 2013, consulte [ligações para o Excel a partir da DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md).</span><span class="sxs-lookup"><span data-stu-id="cb175-109">For more information about calling Excel 2013 functions, see [Calling into Excel from the DLL or XLL](calling-into-excel-from-the-dll-or-xll.md).</span></span>
    
- <span data-ttu-id="cb175-110">**Funções assíncronas definidas pelo usuário**</span><span class="sxs-lookup"><span data-stu-id="cb175-110">**Asynchronous User-defined Functions**</span></span>
    
    <span data-ttu-id="cb175-111">Excel 2013 suporta chamando funções definidas pelo usuário (UDF) de forma assíncrona, que podem melhorar o desempenho, permitindo que vários cálculos executar ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="cb175-111">Excel 2013 supports calling user-defined functions (UDF) asynchronously, which can improve performance by enabling several calculations to run at the same time.</span></span> <span data-ttu-id="cb175-112">Para obter mais informações sobre UDFs assíncronos, consulte [Asynchronous User-Defined funções](asynchronous-user-defined-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cb175-112">For more information about asynchronous UDFs, see [Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md).</span></span>
    
- <span data-ttu-id="cb175-113">**Conectores de cluster**</span><span class="sxs-lookup"><span data-stu-id="cb175-113">**Cluster Connectors**</span></span>
    
    <span data-ttu-id="cb175-114">Conectores de cluster habilitar UDFs executar em clusters de computação de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="cb175-114">Cluster connectors enable UDFs to run on high-performance compute clusters.</span></span> <span data-ttu-id="cb175-115">Para obter mais informações sobre a criação de conectores de cluster, consulte [Desenvolvendo conectores de Cluster do Excel](developing-excel-cluster-connectors.md).</span><span class="sxs-lookup"><span data-stu-id="cb175-115">For more information about creating cluster connectors, see [Developing Excel Cluster Connectors](developing-excel-cluster-connectors.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="cb175-116">Suplementos XLL que você pretende executar em clusters de computadores devem chamar apenas as funções de cluster-safe.</span><span class="sxs-lookup"><span data-stu-id="cb175-116">XLL add-ins that you intend to run on compute clusters must call only cluster-safe functions.</span></span> <span data-ttu-id="cb175-117">Para obter mais informações sobre as funções, você pode usar, consulte [Referência de função de API do Excel XLL SDK](excel-xll-sdk-api-function-reference.md) e [Funções de segurança do Cluster](cluster-safe-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cb175-117">For more information about the functions you can use, see [Excel XLL SDK API Function Reference](excel-xll-sdk-api-function-reference.md) and [Cluster Safe Functions](cluster-safe-functions.md).</span></span> 
  
- <span data-ttu-id="cb175-118">**Suporte de 64 bits**</span><span class="sxs-lookup"><span data-stu-id="cb175-118">**64-bit Support**</span></span>
    
    <span data-ttu-id="cb175-119">Agora você pode compilar e vincular XLLs de 32 bits e 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cb175-119">You can now compile and link both 32-bit and 64-bit XLLs.</span></span> <span data-ttu-id="cb175-120">Para obter mais informações, consulte [Criando XLLs](creating-xlls.md).</span><span class="sxs-lookup"><span data-stu-id="cb175-120">For more information, see [Creating XLLs](creating-xlls.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb175-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb175-121">See also</span></span>



[<span data-ttu-id="cb175-122">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="cb175-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="cb175-123">Programar com a API de C no Excel</span><span class="sxs-lookup"><span data-stu-id="cb175-123">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
[<span data-ttu-id="cb175-124">Vários threads e contenção da memória no Excel</span><span class="sxs-lookup"><span data-stu-id="cb175-124">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)


[<span data-ttu-id="cb175-125">Getting Started with the Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="cb175-125">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

