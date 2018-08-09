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
- função tempactiverow [excel 2007], função TempActiveRow12 [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765434"
---
# <a name="tempactiverowtempactiverow12"></a><span data-ttu-id="e98b1-104">TempActiveRow/TempActiveRow12</span><span class="sxs-lookup"><span data-stu-id="e98b1-104">TempActiveRow/TempActiveRow12</span></span>

 <span data-ttu-id="e98b1-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e98b1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e98b1-106">Funções da biblioteca Framework que criam um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa para uma linha inteira na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="e98b1-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire row on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a><span data-ttu-id="e98b1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e98b1-107">Parameters</span></span>

 <span data-ttu-id="e98b1-108">_row_</span><span class="sxs-lookup"><span data-stu-id="e98b1-108">_row_</span></span>
  
<span data-ttu-id="e98b1-109">A linha a ser referenciado.</span><span class="sxs-lookup"><span data-stu-id="e98b1-109">The row to be referenced.</span></span> <span data-ttu-id="e98b1-110">Argumentos de linha são baseada em zero, portanto, essa linha 1 é passada como 0.</span><span class="sxs-lookup"><span data-stu-id="e98b1-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="e98b1-111">No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é 65.535 = 2 ^ 16-1 e é o valor máximo que pode ser realizado por um inteiro do WORD.</span><span class="sxs-lookup"><span data-stu-id="e98b1-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="e98b1-112">Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="e98b1-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="e98b1-113">RW é definido como um inteiro assinado de 32 bits em XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="e98b1-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="e98b1-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e98b1-114">Return value</span></span>

<span data-ttu-id="e98b1-115">Retorna uma referência de **xltypeRef** externo às células da linha passados.</span><span class="sxs-lookup"><span data-stu-id="e98b1-115">Returns an **xltypeRef** external reference to row cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e98b1-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e98b1-116">Example</span></span>

<span data-ttu-id="e98b1-117">Este exemplo usa a função **TempActiveRow12** para selecionar linha 113.</span><span class="sxs-lookup"><span data-stu-id="e98b1-117">This example uses the **TempActiveRow12** function to select row 113.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="e98b1-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e98b1-118">See also</span></span>



[<span data-ttu-id="e98b1-119">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="e98b1-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

