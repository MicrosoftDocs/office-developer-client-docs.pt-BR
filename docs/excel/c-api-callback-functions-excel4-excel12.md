---
title: O retorno de chamada do C API funciona Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [excel 2007], o retorno de chamada de api c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 221ea4c9c706d11acd31d3f2870d326a7189d299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765249"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="0878f-104">O retorno de chamada do C API funciona Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="0878f-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="0878f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0878f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0878f-106">As funções do **Excel4** e **Excel12** são fornecidas para habilitar DLLs chamar uma função de planilha do Microsoft Excel interna, função de folha de macro ou comando, ou somente XLL função especial ou comando.</span><span class="sxs-lookup"><span data-stu-id="0878f-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="0878f-107">A função **Excel4** suportam a todas as versões recentes do Excel.</span><span class="sxs-lookup"><span data-stu-id="0878f-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="0878f-108">Iniciando no Excel 2007 a função **Excel12** é suportado.</span><span class="sxs-lookup"><span data-stu-id="0878f-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="0878f-109">Ambas as funções são fornecidas em duas formas:</span><span class="sxs-lookup"><span data-stu-id="0878f-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="0878f-110">Um formulário de lista de argumentos de comprimento variável (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="0878f-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="0878f-111">Um formulário de matriz de argumentos (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="0878f-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="0878f-112">Com exceção da maneira na qual os argumentos são passados para esses retornos de chamada, as duas formas são funcionalmente equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0878f-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="0878f-113">Os conceitos básicos para ambos os formulários totalmente são descritos na [Excel4/Excel12](excel4-excel12.md).</span><span class="sxs-lookup"><span data-stu-id="0878f-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="0878f-114">[Excel4v/Excel12v](excel4v-excel12v.md) aborda outras questões sobre este formulário.</span><span class="sxs-lookup"><span data-stu-id="0878f-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0878f-115">Nesta se��o</span><span class="sxs-lookup"><span data-stu-id="0878f-115">In this section</span></span>

[<span data-ttu-id="0878f-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="0878f-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="0878f-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="0878f-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

