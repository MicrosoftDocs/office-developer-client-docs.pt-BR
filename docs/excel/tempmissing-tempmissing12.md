---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- função tempmissing [excel 2007], função TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765445"
---
# <a name="tempmissingtempmissing12"></a><span data-ttu-id="83604-104">TempMissing/TempMissing12</span><span class="sxs-lookup"><span data-stu-id="83604-104">TempMissing/TempMissing12</span></span>

 <span data-ttu-id="83604-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="83604-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="83604-106">Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** do tipo **xltypeMissing**.</span><span class="sxs-lookup"><span data-stu-id="83604-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** of type **xltypeMissing**.</span></span>
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a><span data-ttu-id="83604-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83604-107">Parameters</span></span>

<span data-ttu-id="83604-108">Essa função não usa parâmetros.</span><span class="sxs-lookup"><span data-stu-id="83604-108">This function takes no parameters.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="83604-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="83604-109">Return value</span></span>

<span data-ttu-id="83604-110">Retorna um ponteiro para uma **xltypeMissing** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="83604-110">Returns a pointer to an **xltypeMissing** **XLOPER**/ **XLOPER12**.</span></span>
  
## <a name="example"></a><span data-ttu-id="83604-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="83604-111">Example</span></span>

<span data-ttu-id="83604-112">Este exemplo usa **TempMissing12** para fornecer três argumentos ausentes para **xlcWorkspace** seguido **booleano** **FALSE** para suprimir a exibição das barras de rolagem da planilha.</span><span class="sxs-lookup"><span data-stu-id="83604-112">This example uses **TempMissing12** to provide three missing arguments to **xlcWorkspace** followed by a **Boolean** **FALSE** to suppress the display of worksheet scroll bars.</span></span> <span data-ttu-id="83604-113">Os três primeiros argumentos correspondem às outras configurações de espaço de trabalho que não são afetadas.</span><span class="sxs-lookup"><span data-stu-id="83604-113">The first three arguments correspond to other workspace settings which are unaffected.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="83604-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="83604-114">See also</span></span>



[<span data-ttu-id="83604-115">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="83604-115">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

