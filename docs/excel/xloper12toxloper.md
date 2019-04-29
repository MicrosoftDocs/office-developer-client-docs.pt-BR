---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- função xloper12toxloper [Excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 148353dcec1cc051aa44d18c0a081b6623e3759a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422905"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rotina de conversão usada para converter do novo **XLOPER12** para o antigo **XLOPER**.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parâmetros

_pxloper12_ (**LPXLOPER12**)
  
Ponteiro para a fonte **XLOPER12** a ser convertido. 
  
_pxloper_ (**LPXLOPER**)
  
Ponteiro para o **XLOPER** de destino para conter o valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

**True** se a conversão tiver sido bem-sucedida; caso contrário, **false** . 
  
## <a name="remarks"></a>Comentários

Dependendo do tipo de **XLOPER12**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para o **XLOPER**de destino. O chamador é responsável por liberar qualquer memória associada à cópia se a conversão for bem-sucedida; O **FreeXLOperT** pode ser usado ou pode ser feito diretamente usando o **gratuitamente**.
  
Se a conversão falhar, o chamador não precisará liberar memória.
  
Conversão de um **XLOPER12** para um **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência que é muito grande ou uma cadeia de caracteres que é muito longa para o **XLOPER** conter. 
  
**XLOPER12** As cadeias de caracteres largos Unicode **** são convertidas em cadeias de caracteres de bytes ASCII de tamanho, de forma que seja dependente da localidade. 
  
O **** **xltypeInt** XLOPER12 é um inteiro assinado de 32 bits, enquanto o **XLOPER** **xltypeInt** é um inteiro assinado de 16 bits. Quando um inteiro **XLOPER12** fornecido exceder o limite de um inteiro **XLOPER** , o inteiro é convertido em um Double de 8 bytes e retornado em um **XLOPER** do tipo **xltypeNum**. Este é o único caso em que essa função altera o tipo de **XLOPER**convertido.
  
### <a name="example"></a>Exemplo

ConFira o `\SAMPLES\FRAMEWRK\FRAMEWRK.C` arquivo para o código da função. 
  
## <a name="see-also"></a>Confira também

- [Funções na biblioteca do Framework](functions-in-the-framework-library.md)

