---
title: Desenvolvendo XLLs do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- suplementos - [excel 2007], desenvolvendo XLLs XLLs - [Excel 2007] - [Excel 2007], desenvolvendo
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765272"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="b993a-104">Desenvolvendo XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="b993a-104">Developing Excel XLLs</span></span>

<span data-ttu-id="b993a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b993a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b993a-106">O principal motivo para escrever XLLs do Microsoft Excel e usando a API C é criar funções de planilha de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="b993a-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="b993a-107">Os aplicativos de funções de alto desempenho — e, iniciando no Excel 2007, a capacidade de gravar interfaces multithreaded aos recursos de servidor poderosas — tornam uma parte muito importante de extensibilidade do Excel.</span><span class="sxs-lookup"><span data-stu-id="b993a-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="b993a-108">O desempenho dos XLLs ainda mais foi aprimorado no Excel 2007 pela adição de novos tipos de dados e, mais importante, suporte para multithreading.</span><span class="sxs-lookup"><span data-stu-id="b993a-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="b993a-109">A API C não tem nenhum dos recursos de desenvolvimento rápido de nível superior do Microsoft Visual Basic for Applications (VBA), COM ou o Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="b993a-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="b993a-110">Gerenciamento de memória é baixo nível e, portanto, lança a responsabilidade de maior sobre o desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="b993a-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="b993a-111">Muitos recursos do Excel que são expostos por meio de COM, torná-los disponíveis por meio do VBA e o .NET Framework, não estão expostos a API C.</span><span class="sxs-lookup"><span data-stu-id="b993a-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="b993a-112">Excel Programming Concepts</span><span class="sxs-lookup"><span data-stu-id="b993a-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="b993a-113">Trabalhando com DLLs</span><span class="sxs-lookup"><span data-stu-id="b993a-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="b993a-114">Acessando código XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="b993a-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="b993a-115">Funções do Assistente de função ou caixas de diálogo Replace XLL chamada</span><span class="sxs-lookup"><span data-stu-id="b993a-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="b993a-116">Calling into Excel from the DLL or XLL</span><span class="sxs-lookup"><span data-stu-id="b993a-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="b993a-117">Criando XLLs</span><span class="sxs-lookup"><span data-stu-id="b993a-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="b993a-118">Avaliando os nomes e outras expressões de fórmula de planilha</span><span class="sxs-lookup"><span data-stu-id="b993a-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="b993a-119">Multithreading e gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="b993a-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="b993a-120">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="b993a-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="b993a-121">Funções de segurança de cluster</span><span class="sxs-lookup"><span data-stu-id="b993a-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="b993a-122">Quebras de autorizações de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="b993a-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="b993a-123">Exibindo caixas de diálogo de dentro de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="b993a-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="b993a-124">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="b993a-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="b993a-125">Compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="b993a-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

