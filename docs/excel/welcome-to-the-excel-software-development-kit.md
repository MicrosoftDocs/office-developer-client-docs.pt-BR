---
title: Bem-vindo ao Software Development Kit do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- excel 2007 xll software development kit,add-ins [Excel 2007]
localization_priority: Normal
ms.assetid: abfc9d76-6f22-49b9-ba45-eb7a54b082e0
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4de88a12b5fb945c6243e52b77babe88b2d02417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765446"
---
# <a name="welcome-to-the-excel-software-development-kit"></a><span data-ttu-id="92828-104">Bem-vindo ao Software Development Kit do Excel</span><span class="sxs-lookup"><span data-stu-id="92828-104">Welcome to the Excel Software Development Kit</span></span>

 <span data-ttu-id="92828-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="92828-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="92828-p101">Bem-vindo � documenta��o do Excel 2013 Software Development Kit (SDK). Esta refer�ncia cont�m uma vis�o geral, algumas tarefas de programa��o e exemplos para ajud�-lo a desenvolver XLLs do Microsoft Excel 2013.</span><span class="sxs-lookup"><span data-stu-id="92828-p101">Welcome to the Excel 2013 XLL Software Development Kit (SDK) documentation. This reference contains conceptual overviews, programming tasks, and samples to help you develop Microsoft Excel 2013 XLLs.</span></span>
  
<span data-ttu-id="92828-108">Revisado em: Novembro de 2012</span><span class="sxs-lookup"><span data-stu-id="92828-108">Revised: November 2012</span></span>
  
<span data-ttu-id="92828-109">Baixe o [Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082).</span><span class="sxs-lookup"><span data-stu-id="92828-109">Download the [Excel 2013 XLL SDK](http://go.microsoft.com/fwlink/?LinkID=251082).</span></span>
  
<span data-ttu-id="92828-110">O Excel 2013 XLL SDK inclui:</span><span class="sxs-lookup"><span data-stu-id="92828-110">The Excel 2013 XLL SDK includes the following:</span></span>
  
- <span data-ttu-id="92828-111">**Interface de programa��o de aplicativo (API) C** � inclui arquivos de origem e de cabe�alho que permitem que os DLLs acessem a funcionalidade do Excel 2013 e uma descri��o da interface que uma DLL deve expor para trabalhar com o Gerenciador de Suplementos do Excel.</span><span class="sxs-lookup"><span data-stu-id="92828-111">**C application programming interface (API)**—Includes header and source files that enable DLLs to access Excel 2013 functionality, and a description of the interface that a DLL should expose to work with the Excel Add-in Manager.</span></span>
    
- <span data-ttu-id="92828-p102">**Projetos do Microsoft Visual Studio** � inclui c�digo-fonte C/C++ e mostra como usar a API C. Esses projetos de amostragem fornecem exemplos e servem como ponto de partida para que voc� desenvolva seu pr�prio suplemento.</span><span class="sxs-lookup"><span data-stu-id="92828-p102">**Microsoft Visual Studio projects**—Includes C/C++ source code and shows how to use the C API. These sample projects provide examples and they serve as a starting point for your own add-in development.</span></span>
    
<span data-ttu-id="92828-114">A documenta��o SDK cont�m as seguintes se��es:</span><span class="sxs-lookup"><span data-stu-id="92828-114">The SDK documentation contains the following sections:</span></span>
  
- [<span data-ttu-id="92828-115">Getting Started with the Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="92828-115">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)
    
- [<span data-ttu-id="92828-116">Developing Excel XLLs</span><span class="sxs-lookup"><span data-stu-id="92828-116">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
    
- [<span data-ttu-id="92828-117">Developing Excel Cluster Connectors</span><span class="sxs-lookup"><span data-stu-id="92828-117">Developing Excel Cluster Connectors</span></span>](developing-excel-cluster-connectors.md)
    
- [<span data-ttu-id="92828-118">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="92828-118">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)
    
## <a name="functionality-not-covered"></a><span data-ttu-id="92828-119">Funcionalidade n�o coberta</span><span class="sxs-lookup"><span data-stu-id="92828-119">Functionality Not Covered</span></span>

<span data-ttu-id="92828-120">Os seguintes assuntos n�o ser�o abordados:</span><span class="sxs-lookup"><span data-stu-id="92828-120">The following subjects are not covered:</span></span>
  
- <span data-ttu-id="92828-121">Desenvolvendo comandos e fun��es definidas pelo usu�rio em planilhas de macro do Excel (XLM).</span><span class="sxs-lookup"><span data-stu-id="92828-121">Developing user-defined functions and commands in Excel macro (XLM) sheets.</span></span>
    
- <span data-ttu-id="92828-122">Criando fun��es definidas pelo usu�rio em DLLs que controlam o fluxo de execu��o de uma macro XLM.</span><span class="sxs-lookup"><span data-stu-id="92828-122">Creating user-defined functions in DLLs that control the flow of execution of an XLM macro.</span></span>
    
    <span data-ttu-id="92828-123">Essas fun��es retornam um tipo especial de dados de controle de fluxo, que n�o est� descrito nesta documenta��o.</span><span class="sxs-lookup"><span data-stu-id="92828-123">Such functions work by returning a special flow control data type, which is also not described in this documentation.</span></span>
    
## <a name="related-links"></a><span data-ttu-id="92828-124">Links relacionados</span><span class="sxs-lookup"><span data-stu-id="92828-124">Related Links</span></span>

[<span data-ttu-id="92828-125">Excel Developer Center</span><span class="sxs-lookup"><span data-stu-id="92828-125">Excel Developer Center</span></span>](http://msdn.microsoft.com/pt-br/office/aa905411.aspx)
  
[<span data-ttu-id="92828-126">Centro de Desenvolvimento do Microsoft Office</span><span class="sxs-lookup"><span data-stu-id="92828-126">Microsoft Office Developer Center</span></span>](http://msdn.microsoft.com/pt-br/office/default.aspx)
  
[<span data-ttu-id="92828-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span><span class="sxs-lookup"><span data-stu-id="92828-127">Excel 2010 SDK: Excel 2010 XLL Software Development Kit</span></span>](http://go.microsoft.com/fwlink/?LinkID=186435)
  

