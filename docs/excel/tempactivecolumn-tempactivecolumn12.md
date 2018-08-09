---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- função tempactivecolumn12 [excel 2007], função TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765439"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="c5060-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="c5060-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="c5060-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c5060-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c5060-106">Funções da biblioteca Framework que criam um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa para uma coluna inteira na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="c5060-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="c5060-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5060-107">Parameters</span></span>

 <span data-ttu-id="c5060-108">_col_ (**Bytes**)</span><span class="sxs-lookup"><span data-stu-id="c5060-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="c5060-109">A coluna a ser referenciado.</span><span class="sxs-lookup"><span data-stu-id="c5060-109">The column to be referenced.</span></span> <span data-ttu-id="c5060-110">Isso é baseado em zero que a coluna A é passada como 0.</span><span class="sxs-lookup"><span data-stu-id="c5060-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="c5060-111">No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é de 255 = 2 ^ 8 1 e é o valor máximo que pode ser realizado por um inteiro de bytes.</span><span class="sxs-lookup"><span data-stu-id="c5060-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="c5060-112">Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 16,383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="c5060-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="c5060-113">COL é definido como um inteiro assinado de 32 bits em XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="c5060-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c5060-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c5060-114">Return value</span></span>

<span data-ttu-id="c5060-115">Retorna uma referência de **xltypeRef** externo à coluna passada.</span><span class="sxs-lookup"><span data-stu-id="c5060-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c5060-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c5060-116">Example</span></span>

<span data-ttu-id="c5060-117">O exemplo a seguir usa **TempActiveColumn12** para selecionar toda a coluna B.</span><span class="sxs-lookup"><span data-stu-id="c5060-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c5060-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5060-118">See also</span></span>



[<span data-ttu-id="c5060-119">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="c5060-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

