---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- função Func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765372"
---
# <a name="func1"></a><span data-ttu-id="1211b-104">Func1</span><span class="sxs-lookup"><span data-stu-id="1211b-104">Func1</span></span>

 <span data-ttu-id="1211b-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1211b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1211b-106">Função de planilha definida pelo usuário de exemplo demonstra o retorno de um valor de cadeia de caracteres estática.</span><span class="sxs-lookup"><span data-stu-id="1211b-106">Example user-defined worksheet function demonstrates the return of a static string value.</span></span> <span data-ttu-id="1211b-107">Quando GENERIC.xll é carregado, ele registra esta função para que ele possa ser chamado da planilha.</span><span class="sxs-lookup"><span data-stu-id="1211b-107">When GENERIC.xll is loaded, it registers this function so that it can be called from the worksheet.</span></span>
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a><span data-ttu-id="1211b-108">Par�metros</span><span class="sxs-lookup"><span data-stu-id="1211b-108">Parameters</span></span>

 <span data-ttu-id="1211b-109">_px_ (**LPXLOPER**)</span><span class="sxs-lookup"><span data-stu-id="1211b-109">_px_ (**LPXLOPER**)</span></span>
  
<span data-ttu-id="1211b-110">Este argumento será ignorado e serve apenas para o Microsoft Excel para chamar a função de gatilho.</span><span class="sxs-lookup"><span data-stu-id="1211b-110">This argument is ignored, and serves only to trigger Microsoft Excel to call the function.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="1211b-111">Propriedade valor/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1211b-111">Property value/Return value</span></span>

 <span data-ttu-id="1211b-112">**LPXLOPER12**: sempre é a cadeia de caracteres "Func1"</span><span class="sxs-lookup"><span data-stu-id="1211b-112">**LPXLOPER12**: Always the string "Func1"</span></span>
  
### <a name="example"></a><span data-ttu-id="1211b-113">Example</span><span class="sxs-lookup"><span data-stu-id="1211b-113">Example</span></span>

<span data-ttu-id="1211b-114">Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função.</span><span class="sxs-lookup"><span data-stu-id="1211b-114">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1211b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="1211b-115">See also</span></span>



[<span data-ttu-id="1211b-116">Funções na DLL genérico</span><span class="sxs-lookup"><span data-stu-id="1211b-116">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

