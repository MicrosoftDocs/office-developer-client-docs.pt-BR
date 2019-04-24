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
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de estrutura que tenta converter um **XLREF** em um **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parâmetros

 _pxRef_ (**LPXLREF**)
  
Ponteiro para a estrutura de referência de origem.
  
 _pxRef12_ (**LPXLREF12**)
  
Ponteiro para a estrutura de referência de destino na qual o valor convertido deve ser colocado.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

 **True** se a conversão tiver sido bem-sucedida; caso contrário, **false** . 
  
## <a name="remarks"></a>Comentários

Desde que o **XLREF** passado seja válido, essa operação sempre deverá ser bem-sucedida. Por outro lado, a conversão da outra maneira de **XLREF12** para **XLREF**, realizada pelo [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), falhará se a referência fornecida se referir a parte de uma planilha do Excel 2007 que não tem suporte em versões anteriores.
  
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

