---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- função func1 [Excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304078"
---
# <a name="func1"></a><span data-ttu-id="4636f-104">Func1</span><span class="sxs-lookup"><span data-stu-id="4636f-104">Func1</span></span>

 <span data-ttu-id="4636f-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4636f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4636f-106">Exemplo de função de planilha definida pelo usuário demonstra o retorno de um valor de cadeia de caracteres estática.</span><span class="sxs-lookup"><span data-stu-id="4636f-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="4636f-107">Quando GENERIC. XLL é carregado, ele registra essa função para que ela possa ser chamada da planilha.</span><span class="sxs-lookup"><span data-stu-id="4636f-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="4636f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4636f-108">Parameters</span></span>

 <span data-ttu-id="4636f-109">_PX_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="4636f-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="4636f-110">Esse argumento é ignorado e serve apenas para disparar o Microsoft Excel para chamar a função.</span><span class="sxs-lookup"><span data-stu-id="4636f-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="4636f-111">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4636f-111">Property value/Return value</span></span>

 <span data-ttu-id="4636f-112">**LPXLOPER12**: sempre a cadeia de caracteres "func1"</span><span class="sxs-lookup"><span data-stu-id="4636f-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="4636f-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4636f-113">Example</span></span>

<span data-ttu-id="4636f-114">Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="4636f-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4636f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="4636f-115">See also</span></span>



[<span data-ttu-id="4636f-116">Funções na DLL genérica</span><span class="sxs-lookup"><span data-stu-id="4636f-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

