---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- função xlopertoxloper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765500"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para converter do antigo **XLOPER** o novo **XLOPER12**rotina de conversão.
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Par�metros

_pxloper_ (**LPXLOPER**)
  
Ponteiro para a fonte **XLOPER** a ser convertido. 
  
_pxloper12_ (**LPXLOPER12**)
  
Ponteiro para o destino **XLOPER12** contenha o valor convertido. 
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

**TRUE** se a conversão foi bem-sucedida, **FALSE** caso contrário. 
  
## <a name="remarks"></a>Coment�rios

Dependendo do tipo de **XLOPER**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para no destino **XLOPER12**. O chamador é responsável por liberar qualquer memória associada a cópia se a conversão foi bem sucedida; **FreeXLOper12T** pode ser usado, ou pode ser feito diretamente usando **livre**.
  
Se a conversão falhar, o chamador não precisará liberar qualquer memória.
  
Em geral, a conversão de qualquer **XLOPER** em **XLOPER12** é possível. Por outro lado, a conversão de **XLOPER12** em **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência é muito grande ou uma cadeia de caracteres que é muito longa para **XLOPER** conter. 
  
**XLOPER** Cadeias de caracteres de byte ASCII são convertidas em cadeias de caracteres Unicode **XLOPER12** caractere largo de forma que depende da localidade. 
  
### <a name="example"></a>Example

Consulte o arquivo `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para essa função. 
  

