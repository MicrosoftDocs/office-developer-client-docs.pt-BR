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
- função tempactivecolumn12 [Excel 2007], função TempActiveColumn [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417872"
---
# <a name="tempactivecolumntempactivecolumn12"></a><span data-ttu-id="dd1ba-104">TempActiveColumn/TempActiveColumn12</span><span class="sxs-lookup"><span data-stu-id="dd1ba-104">TempActiveColumn/TempActiveColumn12</span></span>

 <span data-ttu-id="dd1ba-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dd1ba-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dd1ba-106">Funções de biblioteca da estrutura que criam um **XLOPER de XLOPER**/ \*\*\*\* temporário contendo uma referência externa para uma coluna inteira na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-106">Framework library functions that create a temporary **XLOPER**/ **XLOPER12** containing an external reference to an entire column on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a><span data-ttu-id="dd1ba-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd1ba-107">Parameters</span></span>

 <span data-ttu-id="dd1ba-108">_Col_ (**Byte**)</span><span class="sxs-lookup"><span data-stu-id="dd1ba-108">_col_ (**BYTE**)</span></span>
  
<span data-ttu-id="dd1ba-109">A coluna a ser referenciada.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-109">The column to be referenced.</span></span> <span data-ttu-id="dd1ba-110">Isso é baseado em zero, para que A coluna A seja passada como 0.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-110">This is zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="dd1ba-111">No Microsoft Office Excel 2003 e versões anteriores, e a partir do Excel 2007 executando uma pasta de trabalho no modo de compatibilidade, o valor máximo é 255 = 2 ^ 8-1 e é o valor máximo que pode ser feito por um inteiro de BYTE.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-111">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="dd1ba-112">A partir do Excel 2007 executando uma pasta de trabalho, o valor máximo é 16.383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-112">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="dd1ba-113">COL é definido como um inteiro assinado de 32 bits em XLCALL. 0.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-113">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="dd1ba-114">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dd1ba-114">Return value</span></span>

<span data-ttu-id="dd1ba-115">Retorna uma referência externa **xltypeRef** à coluna passada.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-115">Returns an **xltypeRef** external reference to the column passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="dd1ba-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dd1ba-116">Example</span></span>

<span data-ttu-id="dd1ba-117">O exemplo a seguir usa **TempActiveColumn12** para selecionar a coluna inteira B.</span><span class="sxs-lookup"><span data-stu-id="dd1ba-117">The following example uses **TempActiveColumn12** to select the entire column B.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="dd1ba-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd1ba-118">See also</span></span>



[<span data-ttu-id="dd1ba-119">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="dd1ba-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

