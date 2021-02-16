---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- Função xlgethwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425453"
---
# <a name="xlgethwnd"></a><span data-ttu-id="edd3e-104">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="edd3e-104">xlGetHwnd</span></span>

<span data-ttu-id="edd3e-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="edd3e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="edd3e-106">Retorna o alça de janela da janela de nível superior do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="edd3e-106">Returns the window handle of the top-level Microsoft Excel window.</span></span>
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a><span data-ttu-id="edd3e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="edd3e-107">Parameters</span></span>

<span data-ttu-id="edd3e-108">Esta função não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="edd3e-108">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="edd3e-109">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="edd3e-109">Property value/Return value</span></span>

<span data-ttu-id="edd3e-110">Contém a alça de janela (**xltypeInt**) no **campo val.w.**</span><span class="sxs-lookup"><span data-stu-id="edd3e-110">Contains the window handle (**xltypeInt**) in the **val.w** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="edd3e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="edd3e-111">Remarks</span></span>

<span data-ttu-id="edd3e-112">Essa função é útil para escrever código da API do Windows.</span><span class="sxs-lookup"><span data-stu-id="edd3e-112">This function is useful for writing Windows API code.</span></span>
  
<span data-ttu-id="edd3e-113">Quando você chama essa função usando [Excel4](excel4-excel12.md) ou [Excel4v,](excel4v-excel12v.md)a variável de inteiro XLOPER retornada é um int curto de 16 bits assinado. Isso só é capaz de conter os 16 bits baixos do alça do Windows de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="edd3e-113">When you call this function using [Excel4](excel4-excel12.md) or [Excel4v](excel4v-excel12v.md), the returned XLOPER integer variable is a signed 16-bit short int. This is only capable of containing the low 16 bits of the 32-bit Windows handle.</span></span> <span data-ttu-id="edd3e-114">Para encontrar a parte superior, seu código deve iterar por todas as janelas abertas procurando uma combinação com a parte baixa.</span><span class="sxs-lookup"><span data-stu-id="edd3e-114">To find the high part, your code must iterate through all open windows looking for a match with the low part.</span></span> <span data-ttu-id="edd3e-115">A partir do Excel 2007, a variável inteira do **XLOPER12** é um int de 32 bits assinado e, portanto, contém o alça inteira, removendo a necessidade de iterar todas as janelas abertas.</span><span class="sxs-lookup"><span data-stu-id="edd3e-115">Starting in Excel 2007, the integer variable of the **XLOPER12** is a signed 32-bit int and therefore contains the entire handle, removing the need to iterate all open windows.</span></span> 
  
### <a name="example"></a><span data-ttu-id="edd3e-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="edd3e-116">Example</span></span>

<span data-ttu-id="edd3e-117">Consulte o código para a [função fShowDialog](fshowdialog.md) em  `SAMPLES\GENERIC\GENERIC.C` .</span><span class="sxs-lookup"><span data-stu-id="edd3e-117">See the code for the [fShowDialog function](fshowdialog.md) in  `SAMPLES\GENERIC\GENERIC.C`.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="edd3e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="edd3e-118">See also</span></span>

- [<span data-ttu-id="edd3e-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="edd3e-119">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="edd3e-120">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="edd3e-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

