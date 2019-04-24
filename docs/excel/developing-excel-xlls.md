---
title: Desenvolvimento de XLLs do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- suplementos, [excel 2007,] desenvolvendo XLLs - [Excel 2007] - [Excel 2007] desenvolver
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: d05041f2629694c4a96240ea83b6e84b17f9be38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301656"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="1df0b-104">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="1df0b-104">Developing Excel XLLs</span></span>

<span data-ttu-id="1df0b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1df0b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1df0b-106">A principal razão para gravar Microsoft Excel XLLs e usar a API de C é criar funções de planilha de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="1df0b-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="1df0b-107">No entanto, os aplicativos de funções de alto desempenho, e no Excel 2007, a capacidade de gravar interfaces de vários threads em recursos avançados do servidor, fazem disso uma parte muito importante da extensibilidade do Excel.</span><span class="sxs-lookup"><span data-stu-id="1df0b-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="1df0b-108">O desempenho XLLs mais avançado no Excel 2007, a adição de novos tipos de dados e mais importante, suporte para multithread.</span><span class="sxs-lookup"><span data-stu-id="1df0b-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="1df0b-109">A API de C não tem nenhum dos recursos de desenvolvimento rápido do Microsoft Visual Basic para aplicativos (VBA), COM ou Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="1df0b-109">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework.</span></span> <span data-ttu-id="1df0b-110">O gerenciamento de memória é de nível baixo e, portanto, atribui uma maior responsabilidade ao desenvolvedor.</span><span class="sxs-lookup"><span data-stu-id="1df0b-110">Memory management is low level, and therefore puts greater responsibility on the developer.</span></span> <span data-ttu-id="1df0b-111">Muitos recursos do Excel que são expostos pelo COM, tornando-os disponíveis por meio do VBA e o .NET Framework, não são expostos à API de C.</span><span class="sxs-lookup"><span data-stu-id="1df0b-111">Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="1df0b-112">Conceitos de programação do Excel</span><span class="sxs-lookup"><span data-stu-id="1df0b-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="1df0b-113">Trabalhar com DLLs</span><span class="sxs-lookup"><span data-stu-id="1df0b-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- [<span data-ttu-id="1df0b-114">Acessar o código de XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="1df0b-114">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
- [<span data-ttu-id="1df0b-115">Chamar funções de XLL no Assistente de Função ou Substituir nas caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="1df0b-115">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
  
- [<span data-ttu-id="1df0b-116">Chamada para o Excel da DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="1df0b-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="1df0b-117">Como criar XLLs</span><span class="sxs-lookup"><span data-stu-id="1df0b-117">Creating XLLs</span></span>](creating-xlls.md)
  
- [<span data-ttu-id="1df0b-118">Avaliar nomes e outras expressões de fórmula de planilha</span><span class="sxs-lookup"><span data-stu-id="1df0b-118">Evaluating Names and Other Worksheet Formula Expressions</span></span>](evaluating-names-and-other-worksheet-formula-expressions.md)
  
- [<span data-ttu-id="1df0b-119">Gerenciamento de memória e multithreading</span><span class="sxs-lookup"><span data-stu-id="1df0b-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- [<span data-ttu-id="1df0b-120">Funções assíncronas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="1df0b-120">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
  
- [<span data-ttu-id="1df0b-121">Funções seguras para clusters</span><span class="sxs-lookup"><span data-stu-id="1df0b-121">Cluster Safe Functions</span></span>](cluster-safe-functions.md)
  
- [<span data-ttu-id="1df0b-122">Permitir intervenções de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="1df0b-122">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
  
- [<span data-ttu-id="1df0b-123">Exibir caixas de diálogo de dentro de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="1df0b-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="1df0b-124">Acessar a instância do Excel e as alças da janela principal</span><span class="sxs-lookup"><span data-stu-id="1df0b-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="1df0b-125">Compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="1df0b-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

