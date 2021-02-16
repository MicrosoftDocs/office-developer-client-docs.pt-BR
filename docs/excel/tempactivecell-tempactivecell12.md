---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- função tempactivecell12 [excel 2007],função TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413189"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="69b39-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="69b39-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="69b39-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="69b39-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="69b39-106">Funções de biblioteca de estrutura que criam um /  **XLOPER XLOPER12** temporário contendo uma referência externa a uma célula na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="69b39-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="69b39-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69b39-107">Parameters</span></span>

 <span data-ttu-id="69b39-108">_row_</span><span class="sxs-lookup"><span data-stu-id="69b39-108">_row_</span></span>
  
<span data-ttu-id="69b39-109">A linha a ser referenciada.</span><span class="sxs-lookup"><span data-stu-id="69b39-109">The row to be referenced.</span></span> <span data-ttu-id="69b39-110">Os argumentos de linha são baseados em zero para que a linha 1 seja passada como 0.</span><span class="sxs-lookup"><span data-stu-id="69b39-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="69b39-111">No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 65.535 = 2^16 - 1 e é o valor máximo que pode ser feito por um inteiro do WORD.</span><span class="sxs-lookup"><span data-stu-id="69b39-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="69b39-112">A partir do Excel 2007 executando uma planilha, o valor máximo é 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="69b39-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="69b39-113">O RW é definido como um inteiro assinado de 32 bits em XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="69b39-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="69b39-114">_col_</span><span class="sxs-lookup"><span data-stu-id="69b39-114">_col_</span></span>
  
<span data-ttu-id="69b39-115">A coluna a ser referenciada.</span><span class="sxs-lookup"><span data-stu-id="69b39-115">The column to be referenced.</span></span> <span data-ttu-id="69b39-116">Isso é baseado em zero para que a coluna A seja passada como 0.</span><span class="sxs-lookup"><span data-stu-id="69b39-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="69b39-117">No Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 255 = 2^8 - 1 e é o valor máximo que pode ser feito por um inteiro BYTE.</span><span class="sxs-lookup"><span data-stu-id="69b39-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="69b39-118">A partir do Excel 2007 executando uma planilha, o valor máximo é 16.383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="69b39-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="69b39-119">COL é definido como um inteiro assinado de 32 bits em XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="69b39-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="69b39-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="69b39-120">Return value</span></span>

<span data-ttu-id="69b39-121">Retorna uma **referência externa xltypeRef** para a célula passada.</span><span class="sxs-lookup"><span data-stu-id="69b39-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="69b39-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="69b39-122">Example</span></span>

<span data-ttu-id="69b39-123">O exemplo a seguir **usa TempActiveCell12** para exibir o conteúdo de B94 na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="69b39-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="69b39-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="69b39-124">See also</span></span>



[<span data-ttu-id="69b39-125">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="69b39-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

