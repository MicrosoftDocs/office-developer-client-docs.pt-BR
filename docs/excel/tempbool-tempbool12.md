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
- função tempbool [Excel 2007], função TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310350"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca da estrutura que cria **um XLOPER de XLOPER**/ **** temporário contendo **booliano** **true** ou **false**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parâmetros

 _b_ (**int**)
  
Use 0 para retornar **false**; Use qualquer outro valor para retornar **true**.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna um **** **Boolean** xltypeBool contendo o valor lógico passado. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir usa a função **TempBool12** para limpar a barra de status. A memória temporária é liberada quando a função [Excel/Excel12f](excel-excel12f.md) é chamada. 
  
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

