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
- função tempactivecell12 [excel 2007], função TempActiveCell [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765433"
---
# <a name="tempactivecelltempactivecell12"></a><span data-ttu-id="09e28-104">TempActiveCell/TempActiveCell12</span><span class="sxs-lookup"><span data-stu-id="09e28-104">TempActiveCell/TempActiveCell12</span></span>

 <span data-ttu-id="09e28-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="09e28-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="09e28-106">Funções da biblioteca Framework que criam um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa a uma célula na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="09e28-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to a cell on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a><span data-ttu-id="09e28-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09e28-107">Parameters</span></span>

 <span data-ttu-id="09e28-108">_row_</span><span class="sxs-lookup"><span data-stu-id="09e28-108">_row_</span></span>
  
<span data-ttu-id="09e28-109">A linha a ser referenciado.</span><span class="sxs-lookup"><span data-stu-id="09e28-109">The row to be referenced.</span></span> <span data-ttu-id="09e28-110">Argumentos de linha são baseada em zero, portanto, essa linha 1 é passada como 0.</span><span class="sxs-lookup"><span data-stu-id="09e28-110">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="09e28-111">No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é 65.535 = 2 ^ 16-1 e é o valor máximo que pode ser realizado por um inteiro do WORD.</span><span class="sxs-lookup"><span data-stu-id="09e28-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="09e28-112">Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="09e28-112">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="09e28-113">RW é definido como um inteiro assinado de 32 bits em XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="09e28-113">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="09e28-114">_col_</span><span class="sxs-lookup"><span data-stu-id="09e28-114">_col_</span></span>
  
<span data-ttu-id="09e28-115">A coluna a ser referenciado.</span><span class="sxs-lookup"><span data-stu-id="09e28-115">The column to be referenced.</span></span> <span data-ttu-id="09e28-116">Isso é baseado em zero que a coluna A é passada como 0.</span><span class="sxs-lookup"><span data-stu-id="09e28-116">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="09e28-117">No Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é de 255 = 2 ^ 8 1 e é o valor máximo que pode ser realizado por um inteiro de bytes.</span><span class="sxs-lookup"><span data-stu-id="09e28-117">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="09e28-118">Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 16,383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="09e28-118">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="09e28-119">COL é definido como um inteiro assinado de 32 bits em XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="09e28-119">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="09e28-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="09e28-120">Return value</span></span>

<span data-ttu-id="09e28-121">Retorna uma referência de **xltypeRef** externo para a célula passada.</span><span class="sxs-lookup"><span data-stu-id="09e28-121">Returns an **xltypeRef** external reference to the cell passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="09e28-122">Exemplo</span><span class="sxs-lookup"><span data-stu-id="09e28-122">Example</span></span>

<span data-ttu-id="09e28-123">O exemplo a seguir usa **TempActiveCell12** para exibir o conteúdo de B94 na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="09e28-123">The following example uses **TempActiveCell12** to display the contents of B94 on the active sheet.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="09e28-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="09e28-124">See also</span></span>



[<span data-ttu-id="09e28-125">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="09e28-125">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

