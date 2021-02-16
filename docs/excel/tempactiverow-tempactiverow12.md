---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- função tempactiverow [excel 2007],função TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413105"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="6d259-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="6d259-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="6d259-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6d259-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6d259-106">Funções de biblioteca de estrutura que criam um /  **XLOPER XLOPER12** temporário contendo uma referência externa a uma linha inteira na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="6d259-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="6d259-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d259-107">Parameters</span></span>

 <span data-ttu-id="6d259-108">_row_</span><span class="sxs-lookup"><span data-stu-id="6d259-108">_row_</span></span>
  
<span data-ttu-id="6d259-109">A linha a ser referenciada.</span><span class="sxs-lookup"><span data-stu-id="6d259-109">The row to be referenced.</span></span> <span data-ttu-id="6d259-110">Os argumentos de linha são baseados em zero para que a linha 1 seja passada como 0.</span><span class="sxs-lookup"><span data-stu-id="6d259-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="6d259-111">No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 65.535 = 2^16 - 1 e é o valor máximo que pode ser feito por um inteiro do WORD.</span><span class="sxs-lookup"><span data-stu-id="6d259-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="6d259-112">A partir do Excel 2007 executando uma planilha, o valor máximo é 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="6d259-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="6d259-113">O RW é definido como um inteiro assinado de 32 bits em XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="6d259-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6d259-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6d259-114">Return value</span></span>

<span data-ttu-id="6d259-115">Retorna uma **referência externa xltypeRef** para células de linha passadas.</span><span class="sxs-lookup"><span data-stu-id="6d259-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6d259-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6d259-116">Example</span></span>

<span data-ttu-id="6d259-117">Este exemplo usa a **função TempActiveRow12** para selecionar a linha 113.</span><span class="sxs-lookup"><span data-stu-id="6d259-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="6d259-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d259-118">See also</span></span>



[<span data-ttu-id="6d259-119">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="6d259-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

