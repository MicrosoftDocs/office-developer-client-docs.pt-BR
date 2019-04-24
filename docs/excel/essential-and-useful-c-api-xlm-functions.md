---
title: Funções XLM essenciais e úteis da API C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [Excel 2007], c API XLM
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d6acd5bb171fb2494f2adb23584f4e7f088e1b83
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311120"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="2b9c3-104">Funções XLM essenciais e úteis da API C</span><span class="sxs-lookup"><span data-stu-id="2b9c3-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="2b9c3-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2b9c3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2b9c3-106">As funções descritas nesta seção são funções de retorno de chamada do Microsoft Excel que são particularmente úteis para desenvolvedores DLL e XLL.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="2b9c3-107">Desses, a função **xlfRegister** é essencial para XLLs e DLLs que desejam registrar suas funções e comandos para que eles possam ser chamados diretamente do Excel.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="2b9c3-108">As funções **xlfUnregister** e **xlfSetName** são usadas em combinação para cancelar o registro de funções e comandos dll e XLL.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="2b9c3-109">Muito mais funções são expostas pelo Excel por meio da API C que são úteis quando você está desenvolvendo XLLs.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="2b9c3-110">Eles correspondem às funções e funções de planilha do Excel e aos comandos que estão disponíveis em planilhas de macros XLM.</span><span class="sxs-lookup"><span data-stu-id="2b9c3-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="2b9c3-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2b9c3-111">In this section</span></span>

[<span data-ttu-id="2b9c3-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="2b9c3-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="2b9c3-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="2b9c3-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="2b9c3-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="2b9c3-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="2b9c3-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="2b9c3-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="2b9c3-116">xlfRegister (Form 1)</span><span class="sxs-lookup"><span data-stu-id="2b9c3-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="2b9c3-117">xlfRegister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="2b9c3-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="2b9c3-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="2b9c3-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="2b9c3-119">xlfUnregister (Formulário 1)</span><span class="sxs-lookup"><span data-stu-id="2b9c3-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="2b9c3-120">xlfUnregister (Formulário 2)</span><span class="sxs-lookup"><span data-stu-id="2b9c3-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="2b9c3-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="2b9c3-121">xlfSetName</span></span>](xlfsetname.md)
  

