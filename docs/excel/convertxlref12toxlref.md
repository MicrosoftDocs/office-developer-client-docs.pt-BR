---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- Função convertxlref12ndolref [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432650"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="01f11-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="01f11-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="01f11-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="01f11-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="01f11-106">Tenta converter um **XLREF12 em** **um XLREF.**</span><span class="sxs-lookup"><span data-stu-id="01f11-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="01f11-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01f11-107">Parameters</span></span>

 <span data-ttu-id="01f11-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="01f11-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="01f11-109">Ponteiro para a estrutura de referência de origem.</span><span class="sxs-lookup"><span data-stu-id="01f11-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="01f11-110">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="01f11-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="01f11-111">Ponteiro para a estrutura de referência de destino na qual o valor convertido deve ser colocado.</span><span class="sxs-lookup"><span data-stu-id="01f11-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="01f11-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="01f11-112">Property value/Return value</span></span>

 <span data-ttu-id="01f11-113">**TRUE** se a conversão foi bem-sucedida; caso contrário, **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="01f11-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="01f11-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="01f11-114">Remarks</span></span>

<span data-ttu-id="01f11-115">A conversão de **XLREF12** para **XLREF** falhará se a referência fornecida se referir a parte de uma planilha do Excel 2007 que não é suportada em versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="01f11-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="01f11-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="01f11-116">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="01f11-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="01f11-117">See also</span></span>



[<span data-ttu-id="01f11-118">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="01f11-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

