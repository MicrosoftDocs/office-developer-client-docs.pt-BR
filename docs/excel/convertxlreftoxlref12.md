---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- função convertxlreftoxlref12 [Excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310985"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="6b4fd-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="6b4fd-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="6b4fd-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="6b4fd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="6b4fd-106">Função de estrutura que tenta converter um **XLREF** em um **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="6b4fd-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="6b4fd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b4fd-107">Parameters</span></span>

 <span data-ttu-id="6b4fd-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="6b4fd-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="6b4fd-109">Ponteiro para a estrutura de referência de origem.</span><span class="sxs-lookup"><span data-stu-id="6b4fd-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="6b4fd-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="6b4fd-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="6b4fd-111">Ponteiro para a estrutura de referência de destino na qual o valor convertido deve ser colocado.</span><span class="sxs-lookup"><span data-stu-id="6b4fd-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="6b4fd-112">Valor de propriedade/Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6b4fd-112">Property value/Return value</span></span>

 <span data-ttu-id="6b4fd-113">**True** se a conversão tiver sido bem-sucedida; caso contrário, **false** .</span><span class="sxs-lookup"><span data-stu-id="6b4fd-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6b4fd-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b4fd-114">Remarks</span></span>

<span data-ttu-id="6b4fd-115">Desde que o **XLREF** passado seja válido, essa operação sempre deverá ser bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6b4fd-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="6b4fd-116">Por outro lado, a conversão da outra maneira de **XLREF12** para **XLREF**, realizada pelo [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), falhará se a referência fornecida se referir a parte de uma planilha do Excel 2007 que não tem suporte em versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="6b4fd-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="6b4fd-117">Exemplo</span><span class="sxs-lookup"><span data-stu-id="6b4fd-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="6b4fd-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b4fd-118">See also</span></span>



[<span data-ttu-id="6b4fd-119">Funções na biblioteca do Framework</span><span class="sxs-lookup"><span data-stu-id="6b4fd-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

