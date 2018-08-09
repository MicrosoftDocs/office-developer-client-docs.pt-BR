---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- função xloper12toxloper [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765485"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rotina de conversão usada para converter do novo **XLOPER12** **XLOPER**antigo.
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>Parâmetros

_pxloper12_ (**LPXLOPER12**)
  
Ponteiro para a fonte **XLOPER12** a ser convertido. 
  
_pxloper_ (**LPXLOPER**)
  
Ponteiro para o destino **XLOPER** contenha o valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

**TRUE** se a conversão foi bem-sucedida, **FALSE** caso contrário. 
  
## <a name="remarks"></a>Comentários

Dependendo do tipo de **XLOPER12**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para no destino **XLOPER**. O chamador é responsável por liberar qualquer memória associada a cópia se a conversão foi bem sucedida; **FreeXLOperT** pode ser usado, ou ele pode ser feito diretamente usando **livre**.
  
Se a conversão falhar, o chamador não precisará liberar qualquer memória.
  
Conversão de **XLOPER12** em **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência é muito grande ou uma cadeia de caracteres que é muito longa para **XLOPER** conter. 
  
**XLOPER12** Cadeias de caracteres de toda a caracteres Unicode são convertidas em cadeias de caracteres de byte **XLOPER** ASCII em uma maneira isto é dependente de localidade. 
  
O **XLOPER12** **xltypeInt** é um inteiro assinado de 32 bits, enquanto o **XLOPER** **xltypeInt** é um inteiro assinado de 16 bits. Quando um inteiro de **XLOPER12** fornecido excede o limite de um inteiro **XLOPER** , o inteiro é convertido em uma dupla de 8 bytes e retornado em **XLOPER** do tipo **xltypeNum**. Este é o único caso em que essa função altera o tipo de **XLOPER**convertido.
  
### <a name="example"></a>Exemplo

Consulte o arquivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para essa função. 
  
## <a name="see-also"></a>Confira também

- [Funções na biblioteca de estrutura](functions-in-the-framework-library.md)

