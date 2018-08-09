---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- função convertxlreftoxlref12 [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765269"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="75afd-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="75afd-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="75afd-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="75afd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="75afd-106">Função Framework que tenta converter uma **XLREF** em um **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="75afd-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="75afd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75afd-107">Parameters</span></span>

 <span data-ttu-id="75afd-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="75afd-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="75afd-109">Ponteiro para a estrutura de referência da fonte.</span><span class="sxs-lookup"><span data-stu-id="75afd-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="75afd-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="75afd-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="75afd-111">Ponteiro para a estrutura de referência de destino em que o valor convertido é sejam colocadas.</span><span class="sxs-lookup"><span data-stu-id="75afd-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="75afd-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="75afd-112">Property value/Return value</span></span>

 <span data-ttu-id="75afd-113">**TRUE** se a conversão foi bem-sucedida, **FALSE** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="75afd-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="75afd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="75afd-114">Remarks</span></span>

<span data-ttu-id="75afd-115">Desde que no passado **XLREF** for válido, essa operação deve sempre ser bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="75afd-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="75afd-116">Por outro lado, conversão da outra forma de **XLREF12** de **XLREF**, realizado por [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), falhará se a referência fornecida refere-se a parte de uma planilha do Excel 2007 que não é suportada nas versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="75afd-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="75afd-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="75afd-117">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="75afd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="75afd-118">See also</span></span>



[<span data-ttu-id="75afd-119">Funções na biblioteca de estrutura</span><span class="sxs-lookup"><span data-stu-id="75afd-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

