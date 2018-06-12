---
title: Funções de XLM API C essenciais e úteis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [excel 2007], xlm do c api
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765285"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="a72ba-104">Funções de XLM API C essenciais e úteis</span><span class="sxs-lookup"><span data-stu-id="a72ba-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="a72ba-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a72ba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a72ba-106">As funções descritas nesta seção são funções de retorno de chamada do Microsoft Excel que são particularmente úteis para os desenvolvedores DLL e XLL.</span><span class="sxs-lookup"><span data-stu-id="a72ba-106">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers.</span></span> <span data-ttu-id="a72ba-107">Desses, a função **xlfRegister** é essencial para XLLs e DLLs que deseja registrar suas funções e comandos para que eles possam ser chamados diretamente do Excel.</span><span class="sxs-lookup"><span data-stu-id="a72ba-107">Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel.</span></span> <span data-ttu-id="a72ba-108">As funções **xlfUnregister** e **xlfSetName** são usados em combinação para cancelar o registro de comandos e funções DLL e XLL.</span><span class="sxs-lookup"><span data-stu-id="a72ba-108">The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="a72ba-109">Muito mais funções são expostas pelo Excel por meio da API C que são úteis quando você estiver desenvolvendo XLLs.</span><span class="sxs-lookup"><span data-stu-id="a72ba-109">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs.</span></span> <span data-ttu-id="a72ba-110">Elas correspondem à planilha do Excel funções e funções e comandos que estão disponíveis a partir de folhas de macro XLM.</span><span class="sxs-lookup"><span data-stu-id="a72ba-110">They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="a72ba-111">Nesta se��o</span><span class="sxs-lookup"><span data-stu-id="a72ba-111">In this section</span></span>

[<span data-ttu-id="a72ba-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="a72ba-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="a72ba-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="a72ba-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="a72ba-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="a72ba-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="a72ba-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="a72ba-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="a72ba-116">xlfRegister (Form 1)</span><span class="sxs-lookup"><span data-stu-id="a72ba-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="a72ba-117">xlfRegister (formulário 2)</span><span class="sxs-lookup"><span data-stu-id="a72ba-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="a72ba-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="a72ba-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="a72ba-119">xlfUnregister (formulário 1)</span><span class="sxs-lookup"><span data-stu-id="a72ba-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="a72ba-120">xlfUnregister (formulário 2)</span><span class="sxs-lookup"><span data-stu-id="a72ba-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="a72ba-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="a72ba-121">xlfSetName</span></span>](xlfsetname.md)
  

