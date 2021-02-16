---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- Função xloperoper12 [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c881f5d03c732b6594e0750808cfa35a65127ed0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404593"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Rotina de conversão usada para converter do **XLOPER antigo** para o novo **XLOPER12.**
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>Parâmetros

_pxloper_ (**LPXLOPER**)
  
Ponteiro para o **XLOPER de origem** a ser convertido. 
  
_pxloper12_ (**LPXLOPER12**)
  
Ponteiro para o **XLOPER12 de destino** para conter o valor convertido. 
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

**TRUE** se a conversão foi bem-sucedida; caso contrário, **FALSE.** 
  
## <a name="remarks"></a>Comentários

Dependendo do tipo de **XLOPER**, essa função aloca um novo buffer de memória para os valores convertidos, que são apontados para o **XLOPER12 de destino.** O chamador é responsável por liberar qualquer memória associada à cópia se a conversão for um sucesso; **FreeXLOper12T** pode ser usado ou pode ser feito diretamente usando **gratuitamente.**
  
Se a conversão falhar, o chamador não precisará liberar memória.
  
Em geral, a conversão de qualquer **XLOPER** para um **XLOPER12** é possível. Por outro lado, a conversão de um **XLOPER12** para um **XLOPER** pode falhar quando o **XLOPER12** contém uma matriz ou referência muito grande ou uma cadeia de caracteres muito longa para o **XLOPER** conter. 
  
**XLOPER** As cadeias de caracteres de byte ASCII são convertidas em cadeias de caracteres largos Unicode **XLOPER12** de uma forma dependente de localidade. 
  
### <a name="example"></a>Exemplo

Consulte o arquivo  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` para o código para esta função. 
  

