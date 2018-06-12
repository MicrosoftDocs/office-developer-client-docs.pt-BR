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
- função tempactiveref [excel 2007], função TempActiveRef12 [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765436"
---
# <a name="tempactivereftempactiveref12"></a><span data-ttu-id="2046e-104">TempActiveRef/TempActiveRef12</span><span class="sxs-lookup"><span data-stu-id="2046e-104">TempActiveRef/TempActiveRef12</span></span>

 <span data-ttu-id="2046e-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2046e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2046e-106">Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** contendo uma referência externa para bloco retangular de células na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="2046e-106">Framework library function that creates a temporary **XLOPER**/ **XLOPER12** containing an external reference to rectangular block of cells on the active sheet.</span></span> 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a><span data-ttu-id="2046e-107">Par�metros</span><span class="sxs-lookup"><span data-stu-id="2046e-107">Parameters</span></span>

 <span data-ttu-id="2046e-108">_rwFirst_</span><span class="sxs-lookup"><span data-stu-id="2046e-108">_rwFirst_</span></span>
  
<span data-ttu-id="2046e-109">A linha de início da referência.</span><span class="sxs-lookup"><span data-stu-id="2046e-109">The starting row of the reference.</span></span>
  
 <span data-ttu-id="2046e-110">_rwLast_</span><span class="sxs-lookup"><span data-stu-id="2046e-110">_rwLast_</span></span>
  
<span data-ttu-id="2046e-111">A linha final da referência.</span><span class="sxs-lookup"><span data-stu-id="2046e-111">The ending row of the reference.</span></span>
  
<span data-ttu-id="2046e-112">Argumentos de linha são baseada em zero, portanto, essa linha 1 é passada como 0.</span><span class="sxs-lookup"><span data-stu-id="2046e-112">Row arguments are zero-based so that row 1 is passed as 0.</span></span> <span data-ttu-id="2046e-113">No Microsoft Office Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é 65.535 = 2 ^ 16-1 e é o valor máximo que pode ser realizado por um inteiro do WORD.</span><span class="sxs-lookup"><span data-stu-id="2046e-113">In Microsoft Office Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 65,535 = 2^16 - 1 and is the maximum value that can be taken by a WORD integer.</span></span> <span data-ttu-id="2046e-114">Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 1.048.575 = 2 ^ 20-1.</span><span class="sxs-lookup"><span data-stu-id="2046e-114">Starting in Excel 2007 running a workbook, the maximum value is 1,048,575 = 2^20 - 1.</span></span> <span data-ttu-id="2046e-115">RW é definido como um inteiro assinado de 32 bits em XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="2046e-115">RW is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
 <span data-ttu-id="2046e-116">_colFirst_</span><span class="sxs-lookup"><span data-stu-id="2046e-116">_colFirst_</span></span>
  
<span data-ttu-id="2046e-117">O número inicial de coluna da referência.</span><span class="sxs-lookup"><span data-stu-id="2046e-117">The starting column number of the reference.</span></span>
  
 <span data-ttu-id="2046e-118">_colLast_</span><span class="sxs-lookup"><span data-stu-id="2046e-118">_colLast_</span></span>
  
<span data-ttu-id="2046e-119">O número de coluna final da referência.</span><span class="sxs-lookup"><span data-stu-id="2046e-119">The ending column number of the reference.</span></span>
  
<span data-ttu-id="2046e-120">Argumentos de coluna estão baseado em zero, portanto, uma coluna é passada como 0.</span><span class="sxs-lookup"><span data-stu-id="2046e-120">Column arguments are zero-based so that column A is passed as 0.</span></span> <span data-ttu-id="2046e-121">No Excel 2003 e anteriores versões e iniciando em uma pasta de trabalho em execução no modo de compatibilidade do Excel 2007, o valor máximo é de 255 = 2 ^ 8 1 e é o valor máximo que pode ser realizado por um inteiro de bytes.</span><span class="sxs-lookup"><span data-stu-id="2046e-121">In Excel 2003 and earlier versions, and starting in Excel 2007 running a workbook in compatibility mode, the maximum value is 255 = 2^8 - 1 and is the maximum value that can be taken by a BYTE integer.</span></span> <span data-ttu-id="2046e-122">Iniciando no Excel 2007 executando uma pasta de trabalho, o valor máximo é 16,383 = 2 ^ 14-1.</span><span class="sxs-lookup"><span data-stu-id="2046e-122">Starting in Excel 2007 running a workbook, the maximum value is 16,383 = 2^14 - 1.</span></span> <span data-ttu-id="2046e-123">COL é definido como um inteiro assinado de 32 bits em XLCALL. H.</span><span class="sxs-lookup"><span data-stu-id="2046e-123">COL is defined as a 32-bit signed integer in XLCALL.H.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="2046e-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2046e-124">Return value</span></span>

<span data-ttu-id="2046e-125">Retorna uma referência de **xltypeRef** externo para bloco retangular de células passados.</span><span class="sxs-lookup"><span data-stu-id="2046e-125">Returns an **xltypeRef** external reference to rectangular block of cells passed in.</span></span> 
  
## <a name="example"></a><span data-ttu-id="2046e-126">Example</span><span class="sxs-lookup"><span data-stu-id="2046e-126">Example</span></span>

<span data-ttu-id="2046e-127">Este exemplo usa a função **TempActiveRef12** para selecionar A105:C110 de células.</span><span class="sxs-lookup"><span data-stu-id="2046e-127">This example uses the **TempActiveRef12** function to select cells A105:C110.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="2046e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2046e-128">See also</span></span>



[<span data-ttu-id="2046e-129">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="2046e-129">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

