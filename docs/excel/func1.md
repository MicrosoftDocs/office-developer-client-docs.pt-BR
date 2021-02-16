---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- função func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408912"
---
# <a name="func1"></a><span data-ttu-id="e78a2-104">Func1</span><span class="sxs-lookup"><span data-stu-id="e78a2-104">Func1</span></span>

 <span data-ttu-id="e78a2-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e78a2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e78a2-106">A função de planilha definida pelo usuário de exemplo demonstra o retorno de um valor estático de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e78a2-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="e78a2-107">Quando GENERIC.xll é carregado, ele registra essa função para que possa ser chamada a partir da planilha.</span><span class="sxs-lookup"><span data-stu-id="e78a2-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="e78a2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e78a2-108">Parameters</span></span>

 <span data-ttu-id="e78a2-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="e78a2-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="e78a2-110">Esse argumento é ignorado e serve apenas para disparar o Microsoft Excel para chamar a função.</span><span class="sxs-lookup"><span data-stu-id="e78a2-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="e78a2-111">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e78a2-111">Property value/Return value</span></span>

 <span data-ttu-id="e78a2-112">**LPXLOPER12**: Sempre a cadeia de caracteres "Func1"</span><span class="sxs-lookup"><span data-stu-id="e78a2-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="e78a2-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e78a2-113">Example</span></span>

<span data-ttu-id="e78a2-114">Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função.</span><span class="sxs-lookup"><span data-stu-id="e78a2-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e78a2-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e78a2-115">See also</span></span>



[<span data-ttu-id="e78a2-116">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="e78a2-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

