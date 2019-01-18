---
title: Bem-vindo ao Software Development Kit do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 365aea48cd520cd368c2a118c832aa705280a308
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708309"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="0c6c8-104">Bem-vindo ao Software Development Kit do Excel</span><span class="sxs-lookup"><span data-stu-id="0c6c8-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="0c6c8-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0c6c8-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0c6c8-p101">Bem-vindo à documentação do Excel 2013 XLL Software Development Kit (SDK). Essa referência contém visões gerais conceituais, tarefas de programação e exemplos para ajudar você a desenvolver Microsoft Excel 2013 XLLs.</span><span class="sxs-lookup"><span data-stu-id="0c6c8-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="0c6c8-108">Revisado em: Novembro de 2012</span><span class="sxs-lookup"><span data-stu-id="0c6c8-108">Revised: November 2012</span></span>
  
<span data-ttu-id="0c6c8-109">Baixe o [Excel 2013 XLL SDK](https://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span><span class="sxs-lookup"><span data-stu-id="0c6c8-109">Download the [Excel 2013 XLL SDK](https://go.microsoft.com/fwlink/?LinkID=251082&amp;clcid=0x409).</span></span>
  
<span data-ttu-id="0c6c8-110">O Excel 2013 XLL SDK inclui:</span><span class="sxs-lookup"><span data-stu-id="0c6c8-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="0c6c8-111">**Interface de programação de aplicativo (API) C** – inclui arquivos de origem e de cabeçalho que permitem que os DLLs acessem a funcionalidade do Excel 2013 e uma descrição da interface que uma DLL deve expor para trabalhar com o Gerenciador de Suplementos do Excel.</span><span class="sxs-lookup"><span data-stu-id="0c6c8-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="0c6c8-p102">**Projetos do Microsoft Visual Studio** – Inclui código fonte C/C++ e mostra como usar a API do C. Essas amostras de projetos servem como exemplos e como ponto de partida para o desenvolvimento do seu próprio suplemento.</span><span class="sxs-lookup"><span data-stu-id="0c6c8-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="0c6c8-114">A documentação SDK contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="0c6c8-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="0c6c8-115">Introdução ao Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="0c6c8-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="0c6c8-116">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="0c6c8-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="0c6c8-117">Developing Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="0c6c8-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="0c6c8-118">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="0c6c8-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="0c6c8-119">Funcionalidade não coberta</span><span class="sxs-lookup"><span data-stu-id="0c6c8-119">Functionality Not Covered</span></span>

<span data-ttu-id="0c6c8-120">Os seguintes assuntos não serão abordados:</span><span class="sxs-lookup"><span data-stu-id="0c6c8-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="0c6c8-121">Desenvolvendo comandos e funções definidas pelo usuário em planilhas de macro do Excel (XLM).</span><span class="sxs-lookup"><span data-stu-id="0c6c8-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="0c6c8-122">Criando funções definidas pelo usuário em DLLs que controlam o fluxo de execução de uma macro XLM.</span><span class="sxs-lookup"><span data-stu-id="0c6c8-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="0c6c8-123">Essas funções retornam um tipo especial de dados de controle de fluxo, que não está descrito nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="0c6c8-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="0c6c8-124">Links relacionados</span><span class="sxs-lookup"><span data-stu-id="0c6c8-124">Related Links</span></span>

[<span data-ttu-id="0c6c8-125">Excel Developer Center</span><span class="sxs-lookup"><span data-stu-id="0c6c8-125">Excel Developer Center</span></span>](https://msdn.microsoft.com/office/aa905411.aspx)
  
[<span data-ttu-id="0c6c8-126">Centro de Desenvolvimento do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="0c6c8-126">Microsoft Office Developer Center</span></span>](https://msdn.microsoft.com/office/default.aspx)
  
[<span data-ttu-id="0c6c8-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span><span class="sxs-lookup"><span data-stu-id="0c6c8-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](https://go.microsoft.com/fwlink/?LinkID=186435&amp;clcid=0x409)
  

