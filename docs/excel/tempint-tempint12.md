---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- função tempint12 [excel 2007], função TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765444"
---
# <a name="tempinttempint12"></a><span data-ttu-id="8e5e4-104">TempInt/TempInt12</span><span class="sxs-lookup"><span data-stu-id="8e5e4-104">TempInt/TempInt12</span></span>

 <span data-ttu-id="8e5e4-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e5e4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8e5e4-106">Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** que contém um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** that contains an integer.</span></span> 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a><span data-ttu-id="8e5e4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e5e4-107">Parameters</span></span>

 <span data-ttu-id="8e5e4-108">_Eu_</span><span class="sxs-lookup"><span data-stu-id="8e5e4-108">_i_</span></span>
  
<span data-ttu-id="8e5e4-109">O valor de inteiro pretendido.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-109">The intended integer value.</span></span> <span data-ttu-id="8e5e4-110">Observe que o inteiro **XLOPER** é um inteiro assinado de 16 bits (short int), enquanto o inteiro **XLOPER12** é um inteiro assinado de 32 bits (int [long]).</span><span class="sxs-lookup"><span data-stu-id="8e5e4-110">Note that the **XLOPER** integer is a signed 16-bit integer (short int), whereas the **XLOPER12** integer is a signed 32-bit integer ([long] int).</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="8e5e4-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8e5e4-111">Return value</span></span>

<span data-ttu-id="8e5e4-112">Retorna um inteiro **xltypeInt** contendo o valor passado.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-112">Returns an **xltypeInt** integer containing the value passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="8e5e4-113">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8e5e4-113">Example</span></span>

<span data-ttu-id="8e5e4-114">Este exemplo usa a função **TempInt12** para passar um argumento para **xlfGetWorkspace**.</span><span class="sxs-lookup"><span data-stu-id="8e5e4-114">This example uses the **TempInt12** function to pass an argument to **xlfGetWorkspace**.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="8e5e4-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e5e4-115">See also</span></span>



[<span data-ttu-id="8e5e4-116">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="8e5e4-116">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

