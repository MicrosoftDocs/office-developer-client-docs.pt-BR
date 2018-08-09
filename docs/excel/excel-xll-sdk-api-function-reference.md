---
title: Excel XLL SDK API Function Reference
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- referência de função de API [excel 2007], funções [Excel 2007], referência [Excel 2007], Excel 2007 XLL Software Development Kit, referência
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765366"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="78cc8-104">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="78cc8-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="78cc8-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="78cc8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="78cc8-106">O Microsoft Excel 2013 XLL SDK contém os arquivos de origem para uma biblioteca de Framework projetado para acelerar a elaboração XLLs e dois projetos de amostra, exemplo e genérico.</span><span class="sxs-lookup"><span data-stu-id="78cc8-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="78cc8-107">Esta seção fornece uma referência de função para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="78cc8-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="78cc8-108">Retornos de chamada que chamar XLL do Excel.</span><span class="sxs-lookup"><span data-stu-id="78cc8-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="78cc8-109">XLL retornos de chamada que procura o Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="78cc8-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="78cc8-110">Funções principais dos projetos de amostra e framework.</span><span class="sxs-lookup"><span data-stu-id="78cc8-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="78cc8-111">Projetos de amostra</span><span class="sxs-lookup"><span data-stu-id="78cc8-111">Sample projects</span></span>

<span data-ttu-id="78cc8-112">O SDK XLL do Excel 2013 fornece os arquivos de origem e os arquivos de projeto do Microsoft Visual Studio para os projetos de amostra a seguir:</span><span class="sxs-lookup"><span data-stu-id="78cc8-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="78cc8-113">O projeto **Framework** (`SAMPLES\FRAMEWRK\`) contém um projeto que pode ser criado em uma biblioteca de FRAMEWRK.lib, que podem ser vinculados, em seguida, em outros projetos XLL.</span><span class="sxs-lookup"><span data-stu-id="78cc8-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="78cc8-114">A biblioteca contém muitas funções e ferramentas que tornam escrever XLLs mais fácil.</span><span class="sxs-lookup"><span data-stu-id="78cc8-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="78cc8-115">Esta biblioteca é usada em ambos os outros projetos em conjunto com o arquivo de cabeçalho FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="78cc8-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="78cc8-116">O projeto de **exemplo** (`SAMPLES\EXAMPLE\`) contém um projeto que pode ser criado para um XLL, EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="78cc8-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="78cc8-117">XLL contém muitos exemplos de implementações de exemplo as funções de interface de Suplemento XLL como **xlAutoOpen**e o uso da biblioteca do Framework.</span><span class="sxs-lookup"><span data-stu-id="78cc8-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="78cc8-118">O projeto **genérico** (`SAMPLES\GENERIC\`) contém um projeto que pode ser criado para um XLL, GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="78cc8-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="78cc8-119">XLL demonstra as várias funções de exemplo e comandos e é um bom ponto de partida para escrever seus próprios XLLs.</span><span class="sxs-lookup"><span data-stu-id="78cc8-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="78cc8-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="78cc8-120">In this section</span></span>

- [<span data-ttu-id="78cc8-121">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="78cc8-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="78cc8-122">C API Callback Functions Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="78cc8-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="78cc8-123">Funções XLM essenciais e úteis para a API de C</span><span class="sxs-lookup"><span data-stu-id="78cc8-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="78cc8-124">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="78cc8-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="78cc8-125">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="78cc8-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="78cc8-126">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="78cc8-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="78cc8-127">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="78cc8-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="78cc8-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="78cc8-128">See also</span></span>

- [<span data-ttu-id="78cc8-129">Programar com a API de C no Excel</span><span class="sxs-lookup"><span data-stu-id="78cc8-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="78cc8-130">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="78cc8-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

