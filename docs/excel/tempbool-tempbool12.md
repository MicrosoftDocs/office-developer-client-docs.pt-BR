---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- função tempbool [excel 2007], função TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765438"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** contendo **Boolean** **TRUE** ou **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Par�metros

 _b_ (**int**)
  
Use 0 para retornar **FALSE**; Use qualquer outro valor para retornar **TRUE**.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Retorna um **xltypeBool** **booliano** que contém o valor lógico passado. 
  
## <a name="example"></a>Example

O exemplo a seguir usa a função **TempBool12** para limpar a barra de status. Memória temporária é liberada quando a função do [Excel/Excel12f](excel-excel12f.md) é chamada. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

