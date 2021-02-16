---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- Função xlgethwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ab4ac1bc040ef2ea9bca182624111e03722c5200
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425453"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o alça de janela da janela de nível superior do Microsoft Excel.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parâmetros

Esta função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Contém a alça de janela (**xltypeInt**) no **campo val.w.** 
  
## <a name="remarks"></a>Comentários

Essa função é útil para escrever código da API do Windows.
  
Quando você chama essa função usando [Excel4](excel4-excel12.md) ou [Excel4v,](excel4v-excel12v.md)a variável de inteiro XLOPER retornada é um int curto de 16 bits assinado. Isso só é capaz de conter os 16 bits baixos do alça do Windows de 32 bits. Para encontrar a parte superior, seu código deve iterar por todas as janelas abertas procurando uma combinação com a parte baixa. A partir do Excel 2007, a variável inteira do **XLOPER12** é um int de 32 bits assinado e, portanto, contém o alça inteira, removendo a necessidade de iterar todas as janelas abertas. 
  
### <a name="example"></a>Exemplo

Consulte o código para a [função fShowDialog](fshowdialog.md) em  `SAMPLES\GENERIC\GENERIC.C` .
  
## <a name="see-also"></a>Confira também

- [xlGetInst](xlgetinst.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

