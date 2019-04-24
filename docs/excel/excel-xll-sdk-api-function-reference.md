---
title: Excel XLL SDK API Function Reference
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304120"
---
# <a name="excel-xll-sdk-api-function-reference"></a><span data-ttu-id="c3b4a-104">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="c3b4a-104">Excel XLL SDK API Function Reference</span></span>

<span data-ttu-id="c3b4a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c3b4a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c3b4a-106">O SDK do Microsoft Excel 2013 XLL contém arquivos de origem para uma biblioteca do Framework que é projetada para acelerar a gravação de XLLs e dois exemplos de projetos, Exemplo e Genérico.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-106">The Microsoft Excel 2013 XLL SDK contains source files for a Framework library that is designed to speed up the writing of XLLs, and two sample projects, Example and Generic.</span></span> 
  
<span data-ttu-id="c3b4a-107">Esta seção fornece uma referência de função para o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c3b4a-107">This section provides a function reference for the following:</span></span>
  
- <span data-ttu-id="c3b4a-108">Retornos de chamada do Excel que o XLL pode chamar.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-108">Excel callbacks that the XLL can call.</span></span>
    
- <span data-ttu-id="c3b4a-109">Retornos de chamada do XLL que o Microsoft Excel procura.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-109">XLL callbacks that Microsoft Excel looks for.</span></span>
    
- <span data-ttu-id="c3b4a-110">Principais funções nas estruturas e projetos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-110">Key functions in the sample and framework projects.</span></span>
    
## <a name="sample-projects"></a><span data-ttu-id="c3b4a-111">Projetos de exemplo</span><span class="sxs-lookup"><span data-stu-id="c3b4a-111">Sample projects</span></span>

<span data-ttu-id="c3b4a-112">O SDK do Excel 2013 XLL fornece arquivos de origem e arquivos de projeto do Microsoft Visual Studio para os seguintes projetos de exemplo:</span><span class="sxs-lookup"><span data-stu-id="c3b4a-112">The Excel 2013 XLL SDK provides source files and Microsoft Visual Studio project files for the following sample projects:</span></span>
  
- <span data-ttu-id="c3b4a-113">O projeto do **Framework** (`SAMPLES\FRAMEWRK\`) contém um projeto que pode ser criado em uma biblioteca, FRAMEWRK.lib, que pode ser vinculado a outros projetos do XLL.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-113">The **Framework** project (`SAMPLES\FRAMEWRK\`) contains a project that can be built to a library, FRAMEWRK.lib, which can then be linked into other XLL projects.</span></span> <span data-ttu-id="c3b4a-114">A biblioteca contém muitas funções e ferramentas para facilitar a gravação de XLLs.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-114">The library contains many functions and tools that make writing XLLs easier.</span></span> <span data-ttu-id="c3b4a-115">Essa biblioteca é usada nos outros dois projetos juntamente com o arquivo de cabeçalho FRAMEWRK.h.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-115">This library is used in both of the other projects in conjunction with the header file FRAMEWRK.h.</span></span>
    
- <span data-ttu-id="c3b4a-116">O projeto de **Exemplo** (`SAMPLES\EXAMPLE\`) contém um projeto que pode ser criado para um XLL, EXAMPLE.xll.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-116">The **Example** project (`SAMPLES\EXAMPLE\`) contains a project that can be built to an XLL, EXAMPLE.xll.</span></span> <span data-ttu-id="c3b4a-117">O XLL contém muitos exemplos do uso da biblioteca do Framework e exemplos de implementações das funções de interface do suplemento XLL, como **xlAutoOpen**.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-117">The XLL contains many examples of the use of the Framework library, and example implementations of the XLL add-in interface functions such as **xlAutoOpen**.</span></span>
    
- <span data-ttu-id="c3b4a-118">O projeto de **Genérico** (`SAMPLES\GENERIC\`) contém um projeto que pode ser criado para um XLL, GENERIC.xll.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-118">The **Generic** project (`SAMPLES\GENERIC\`) contains a project that can be built to an XLL, GENERIC.xll.</span></span> <span data-ttu-id="c3b4a-119">O XLL demonstra várias funções e comandos de exemplo e é um bom ponto de partida para gravar seus próprios XLLs.</span><span class="sxs-lookup"><span data-stu-id="c3b4a-119">The XLL demonstrates several example functions and commands and is a good starting point for writing your own XLLs.</span></span>
    
## <a name="in-this-section"></a><span data-ttu-id="c3b4a-120">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c3b4a-120">In this section</span></span>

- [<span data-ttu-id="c3b4a-121">Gerenciador de Suplemento e Funções da Interface XLL</span><span class="sxs-lookup"><span data-stu-id="c3b4a-121">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)
  
- [<span data-ttu-id="c3b4a-122">Retorno de chamada da API de C: funções Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="c3b4a-122">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)
  
- [<span data-ttu-id="c3b4a-123">Funções XLM essenciais e úteis para a API C</span><span class="sxs-lookup"><span data-stu-id="c3b4a-123">Essential and Useful C API XLM Functions</span></span>](essential-and-useful-c-api-xlm-functions.md)
  
- [<span data-ttu-id="c3b4a-124">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="c3b4a-124">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [<span data-ttu-id="c3b4a-125">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="c3b4a-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)
  
- [<span data-ttu-id="c3b4a-126">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="c3b4a-126">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)
  
- [<span data-ttu-id="c3b4a-127">Funções de conector de cluster do Excel</span><span class="sxs-lookup"><span data-stu-id="c3b4a-127">Excel Cluster Connector Functions</span></span>](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a><span data-ttu-id="c3b4a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3b4a-128">See also</span></span>

- [<span data-ttu-id="c3b4a-129">Programação com a API de C no Excel</span><span class="sxs-lookup"><span data-stu-id="c3b4a-129">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
  
- [<span data-ttu-id="c3b4a-130">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="c3b4a-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

