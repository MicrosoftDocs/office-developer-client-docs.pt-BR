---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- função tempactiveref [excel 2007],função TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415541"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="c20e6-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="c20e6-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="c20e6-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c20e6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c20e6-106">Função de biblioteca de estrutura que cria um /  **XLOPER XLOPER12** temporário contendo uma referência externa ao bloco retangular de células na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="c20e6-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="c20e6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c20e6-107">Parameters</span></span>

 <span data-ttu-id="c20e6-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="c20e6-108">_rwFirst_</span></span>
  
<span data-ttu-id="c20e6-109">A linha inicial da referência.</span><span class="sxs-lookup"><span data-stu-id="c20e6-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="c20e6-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="c20e6-110">_rwLast_</span></span>
  
<span data-ttu-id="c20e6-111">A linha final da referência.</span><span class="sxs-lookup"><span data-stu-id="c20e6-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="c20e6-112">Os argumentos de linha são baseados em zero para que a linha 1 seja passada como 0.</span><span class="sxs-lookup"><span data-stu-id="c20e6-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="c20e6-113">No Microsoft Office Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 65.535 = 2^16 - 1 e é o valor máximo que pode ser feito por um inteiro do WORD.</span><span class="sxs-lookup"><span data-stu-id="c20e6-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="c20e6-114">A partir do Excel 2007 executando uma planilha, o valor máximo é 1.048.575 = 2^20 - 1.</span><span class="sxs-lookup"><span data-stu-id="c20e6-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="c20e6-115">O RW é definido como um inteiro assinado de 32 bits em XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="c20e6-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="c20e6-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="c20e6-116">_colFirst_</span></span>
  
<span data-ttu-id="c20e6-117">O número da coluna inicial da referência.</span><span class="sxs-lookup"><span data-stu-id="c20e6-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="c20e6-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="c20e6-118">_colLast_</span></span>
  
<span data-ttu-id="c20e6-119">O número da coluna final da referência.</span><span class="sxs-lookup"><span data-stu-id="c20e6-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="c20e6-120">Os argumentos de coluna são baseados em zero para que a coluna A seja passada como 0.</span><span class="sxs-lookup"><span data-stu-id="c20e6-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="c20e6-121">No Excel 2003 e em versões anteriores, e a partir do Excel 2007 executando uma planilha no modo de compatibilidade, o valor máximo é 255 = 2^8 - 1 e é o valor máximo que pode ser feito por um inteiro BYTE.</span><span class="sxs-lookup"><span data-stu-id="c20e6-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="c20e6-122">A partir do Excel 2007 executando uma planilha, o valor máximo é 16.383 = 2^14 - 1.</span><span class="sxs-lookup"><span data-stu-id="c20e6-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="c20e6-123">COL é definido como um inteiro assinado de 32 bits em XLCALL.H.</span><span class="sxs-lookup"><span data-stu-id="c20e6-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="c20e6-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c20e6-124">Return value</span></span>

<span data-ttu-id="c20e6-125">Retorna uma **referência externa xltypeRef** para o bloco retangular de células passadas.</span><span class="sxs-lookup"><span data-stu-id="c20e6-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c20e6-126">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c20e6-126">Example</span></span>

<span data-ttu-id="c20e6-127">Este exemplo usa a **função TempActiveRef12** para selecionar as células A105:C110.</span><span class="sxs-lookup"><span data-stu-id="c20e6-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="c20e6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c20e6-128">See also</span></span>



[<span data-ttu-id="c20e6-129">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="c20e6-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

