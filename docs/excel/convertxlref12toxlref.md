---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- função convertxlref12toxlref [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765262"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="875b7-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="875b7-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="875b7-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="875b7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="875b7-106">Tenta converter um **XLREF12** em um **XLREF**.</span><span class="sxs-lookup"><span data-stu-id="875b7-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="875b7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="875b7-107">Parameters</span></span>

 <span data-ttu-id="875b7-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="875b7-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="875b7-109">Ponteiro para a estrutura de referência da fonte.</span><span class="sxs-lookup"><span data-stu-id="875b7-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="875b7-110">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="875b7-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="875b7-111">Ponteiro para a estrutura de referência de destino em que o valor convertido é sejam colocadas.</span><span class="sxs-lookup"><span data-stu-id="875b7-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="875b7-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="875b7-112">Property value/Return value</span></span>

 <span data-ttu-id="875b7-113">**TRUE** se a conversão foi bem-sucedida, **FALSE** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="875b7-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="875b7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="875b7-114">Remarks</span></span>

<span data-ttu-id="875b7-115">A conversão de **XLREF12** para **XLREF** falhará se a referência fornecida refere-se a parte de uma planilha do Excel 2007 que não é suportada nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="875b7-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="875b7-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="875b7-116">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="875b7-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="875b7-117">See also</span></span>



[<span data-ttu-id="875b7-118">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="875b7-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

