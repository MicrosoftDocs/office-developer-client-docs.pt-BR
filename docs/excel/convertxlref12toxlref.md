---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- função convertxlref12toxlref [Excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311050"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Tenta converter um **XLREF12** em um **XLREF**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Parâmetros

 _pxRef12_ (**LPXLREF12**)
  
Ponteiro para a estrutura de referência de origem.
  
 _pxRef_ (**LPXLREF**)
  
Ponteiro para a estrutura de referência de destino na qual o valor convertido deve ser colocado.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

 **True** se a conversão tiver sido bem-sucedida; caso contrário, **false** . 
  
## <a name="remarks"></a>Comentários

A conversão de **XLREF12** para **XLREF** falhará se a referência fornecida se referir a parte de uma planilha do Excel 2007 que não é suportada em versões anteriores. 
  
## <a name="example"></a>Exemplo

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

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

