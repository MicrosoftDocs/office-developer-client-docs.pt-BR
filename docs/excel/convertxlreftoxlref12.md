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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765269"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função Framework que tenta converter uma **XLREF** em um **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Par�metros

 _pxRef_ (**LPXLREF**)
  
Ponteiro para a estrutura de referência da fonte.
  
 _pxRef12_ (**LPXLREF12**)
  
Ponteiro para a estrutura de referência de destino em que o valor convertido é sejam colocadas.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

 **TRUE** se a conversão foi bem-sucedida, **FALSE** caso contrário. 
  
## <a name="remarks"></a>Coment�rios

Desde que no passado **XLREF** for válido, essa operação deve sempre ser bem-sucedidas. Por outro lado, conversão da outra forma de **XLREF12** de **XLREF**, realizado por [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), falhará se a referência fornecida refere-se a parte de uma planilha do Excel 2007 que não é suportada nas versões anteriores.
  
## <a name="example"></a>Exemplo

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

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

