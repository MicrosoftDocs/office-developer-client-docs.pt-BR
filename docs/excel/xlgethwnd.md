---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- função xlGetHwnd [Excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310063"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o identificador de janela da janela do Microsoft Excel de nível superior.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parâmetros

Esta função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Contém o identificador de janela (**xltypeInt**) no campo **Val. w** . 
  
## <a name="remarks"></a>Comentários

Essa função é útil para escrever o código da API do Windows.
  
Ao chamar essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um int de 16 bits com sinal. Isso só é capaz de conter os 16 bits baixos da alça do Windows de 32 bits. Para encontrar a parte superior, seu código deve iterar por todas as janelas abertas procurando uma correspondência com a parte inferior. A partir do Excel 2007, a variável Integer do **XLOPER12** é uma int de 32 bits assinada e, portanto, contém a alça inteira, removendo a necessidade de iterar todas as janelas abertas. 
  
### <a name="example"></a>Exemplo

Consulte o código para a [função fShowDialog](fshowdialog.md) no `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Confira também

- [xlGetInst](xlgetinst.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

