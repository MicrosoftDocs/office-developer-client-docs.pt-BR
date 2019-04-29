---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- função tempbool [Excel 2007], função TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433714"
---
# <a name="tempbooltempbool12"></a><span data-ttu-id="d09c2-104">TempBool/TempBool12</span><span class="sxs-lookup"><span data-stu-id="d09c2-104">TempBool/TempBool12</span></span>

 <span data-ttu-id="d09c2-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d09c2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d09c2-106">Função da biblioteca da estrutura que cria **um XLOPER de XLOPER**/ \*\*\*\* temporário contendo **booliano** **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="d09c2-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing **Boolean** **TRUE** or **FALSE**.</span></span>
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a><span data-ttu-id="d09c2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d09c2-107">Parameters</span></span>

 <span data-ttu-id="d09c2-108">_b_ (**int**)</span><span class="sxs-lookup"><span data-stu-id="d09c2-108">_b_ (**int**)</span></span>
  
<span data-ttu-id="d09c2-109">Use 0 para retornar **false**; Use qualquer outro valor para retornar **true**.</span><span class="sxs-lookup"><span data-stu-id="d09c2-109">Use 0 to return **FALSE**; use any other value to return **TRUE**.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="d09c2-110">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d09c2-110">Property value/Return value</span></span>

<span data-ttu-id="d09c2-111">Retorna um \*\*\*\* **Boolean** xltypeBool contendo o valor lógico passado.</span><span class="sxs-lookup"><span data-stu-id="d09c2-111">Returns an **xltypeBool** **Boolean** containing the logical value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d09c2-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d09c2-112">Example</span></span>

<span data-ttu-id="d09c2-113">O exemplo a seguir usa a função **TempBool12** para limpar a barra de status.</span><span class="sxs-lookup"><span data-stu-id="d09c2-113">The following example uses the **TempBool12** function to clear the status bar.</span></span> <span data-ttu-id="d09c2-114">A memória temporária é liberada quando a função [Excel/Excel12f](excel-excel12f.md) é chamada.</span><span class="sxs-lookup"><span data-stu-id="d09c2-114">Temporary memory is freed when the [Excel/Excel12f](excel-excel12f.md) function is called.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="d09c2-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="d09c2-115">See also</span></span>



[<span data-ttu-id="d09c2-116">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="d09c2-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

