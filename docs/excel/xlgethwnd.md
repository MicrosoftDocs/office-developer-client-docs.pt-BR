---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- função xlGetHwnd [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765487"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o identificador da janela da janela do Microsoft Excel de nível superior.
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Par�metros

Essa função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Contém um manipulador de janela (**xltypeInt**) no campo **val.w** . 
  
## <a name="remarks"></a>Coment�rios

Essa função é útil para escrever o código de API do Windows.
  
Quando você chamar essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um curto int 16 bits assinado, a. Isso só é capaz de conter os 16 bits baixos da alça de Windows de 32 bits. Para localizar a parte alta, seu código deve percorrer todas as janelas abertas procurando uma correspondência com a parte inferior. Iniciando no Excel 2007, a variável de inteiro de **XLOPER12** é um int assinado de 32 bits e, portanto, contém um manipulador de inteiro, removendo a necessidade de iterar todas as janelas abertas. 
  
### <a name="example"></a>Example

Ver o código para a [função fShowDialog](fshowdialog.md) em `SAMPLES\GENERIC\GENERIC.C`.
  
## <a name="see-also"></a>Confira também

- [xlGetInst](xlgetinst.md)
- [Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

