---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- função xlGetHwnd [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310063"
---
# <a name="xlgethwnd"></a><span data-ttu-id="56c15-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="56c15-104">xlGetHwnd</span></span>

<span data-ttu-id="56c15-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="56c15-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="56c15-106">Retorna o identificador de janela da janela do Microsoft Excel de nível superior.</span><span class="sxs-lookup"><span data-stu-id="56c15-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="56c15-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56c15-107">Parameters</span></span>

<span data-ttu-id="56c15-108">Esta função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="56c15-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="56c15-109">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="56c15-109">Property value/Return value</span></span>

<span data-ttu-id="56c15-110">Contém o identificador de janela (**xltypeInt**) no campo **Val. w** .</span><span class="sxs-lookup"><span data-stu-id="56c15-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="56c15-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="56c15-111">Remarks</span></span>

<span data-ttu-id="56c15-112">Essa função é útil para escrever o código da API do Windows.</span><span class="sxs-lookup"><span data-stu-id="56c15-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="56c15-113">Ao chamar essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um int de 16 bits com sinal. Isso só é capaz de conter os 16 bits baixos da alça do Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="56c15-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="56c15-114">Para encontrar a parte superior, seu código deve iterar por todas as janelas abertas procurando uma correspondência com a parte inferior.</span><span class="sxs-lookup"><span data-stu-id="56c15-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="56c15-115">A partir do Excel 2007, a variável Integer do **XLOPER12** é uma int de 32 bits assinada e, portanto, contém a alça inteira, removendo a necessidade de iterar todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="56c15-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="56c15-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="56c15-116">Example</span></span>

<span data-ttu-id="56c15-117">Consulte o código para a [função fShowDialog](fshowdialog.md) no `SAMPLES\GENERIC\GENERIC.C`.</span><span class="sxs-lookup"><span data-stu-id="56c15-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56c15-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="56c15-118">See also</span></span>

- [<span data-ttu-id="56c15-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="56c15-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="56c15-120">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="56c15-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

