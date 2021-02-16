---
title: Retorno de chamada da API de C Funções Excel4, Excel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [excel 2007], retorno de chamada de api c
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5fe5eb7486f12d75ce7e42ad57141480ec735c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434428"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="bfb7d-104">Retorno de chamada da API de C Funções Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="bfb7d-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="bfb7d-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bfb7d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bfb7d-106">As funções **Excel4** e **Excel12** são fornecidas para habilitar DLLs a chamar uma função de planilha interna do Microsoft Excel, função ou comando de planilha de macro ou função especial somente XLL.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-106">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command.</span></span> <span data-ttu-id="bfb7d-107">Todas as versões recentes do Excel suportam **a função Excel4.**</span><span class="sxs-lookup"><span data-stu-id="bfb7d-107">All recent versions of Excel support the **Excel4** function.</span></span> <span data-ttu-id="bfb7d-108">A partir do Excel 2007, a **função Excel12** é suportada.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-108">Starting in Excel 2007 the **Excel12** function is supported.</span></span> <span data-ttu-id="bfb7d-109">Ambas as funções são fornecidas de duas formas:</span><span class="sxs-lookup"><span data-stu-id="bfb7d-109">Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="bfb7d-110">Um formulário de lista de argumentos de comprimento variável (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="bfb7d-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="bfb7d-111">Um formulário de matriz de argumentos (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="bfb7d-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="bfb7d-112">Exceto pela maneira como os argumentos são passados para esses retornos de chamada, os dois formulários são funcionalmente equivalentes.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="bfb7d-113">Os conceitos básicos para ambos os formulários estão totalmente descritos em [Excel4/Excel12.](excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="bfb7d-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="bfb7d-114">[Excel4v/Excel12v](excel4v-excel12v.md) aborda outros problemas sobre este formulário.</span><span class="sxs-lookup"><span data-stu-id="bfb7d-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="bfb7d-115">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bfb7d-115">In this section</span></span>

[<span data-ttu-id="bfb7d-116">Excel4/Excel12</span><span class="sxs-lookup"><span data-stu-id="bfb7d-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="bfb7d-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="bfb7d-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

