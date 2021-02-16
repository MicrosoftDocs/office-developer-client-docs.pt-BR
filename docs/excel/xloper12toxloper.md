---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- Função xloper12esloper [excel 2007]
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
  
Rotina de conversão usada para converter do novo **XLOPER12 para** o **XLOPER antigo.**
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parâmetros

_pxloper12_ (**LPXLOPER12**)
  
Ponteiro para o **XLOPER12** de origem a ser convertido. 
  
_pxloper_ (**LPXLOPER**)
  
Ponteiro para o **XLOPER de destino** para conter o valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

**TRUE** se a conversão foi bem-sucedida; caso contrário, **FALSE.** 
  
## <a name="remarks"></a>Comentários

Dependendo do tipo de **XLOPER12**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para o **XLOPER de** destino. O chamador é responsável por liberar qualquer memória associada à cópia se a conversão for bem-sucedida; **FreeXLOperT** pode ser usado ou pode ser feito diretamente usando **gratuitamente.**
  
Se a conversão falhar, o chamador não precisará liberar memória.
  
A conversão de um **XLOPER12** para um **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência muito grande ou uma cadeia de caracteres muito longa para o **XLOPER** conter. 
  
**XLOPER12** Cadeias de caracteres largos Unicode são convertidas em cadeias de caracteres de byte ASCII **XLOPER** de uma maneira dependente da localidade. 
  
**XlOPER12** **xltypeInt** é um inteiro assinado de 32 bits, enquanto **XLOPER** **xltypeInt** é um inteiro assinado de 16 bits. Quando um inteiro **XLOPER12** fornecido excede o limite de um inteiro **XLOPER,** o inteiro é convertido em um duplo de 8 byte e retornado em um **XLOPER** do tipo **xltypeNum**. Este é o único caso em que essa função altera o tipo do **XLOPER convertido.**
  
### <a name="example"></a>Exemplo

Consulte o arquivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para esta função. 
  
## <a name="see-also"></a>Confira também

- [Funções na biblioteca do Framework](functions-in-the-framework-library.md)

