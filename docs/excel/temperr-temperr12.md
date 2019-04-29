---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- função temperr [Excel 2007], função TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410606"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A função da biblioteca de estrutura que cria um **XLOPER de XLOPER**/ **** temporário contendo um erro de planilha do Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parâmetros

 _err_
  
O código de erro desejado ou seu equivalente numérico literal, conforme mostrado na tabela a seguir.
  
|**Erro**|**Código de erro definido no XLCALL. 0**|**Equivalente Decimal**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |,0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7   <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15   <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |anos  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Valor de retorno

Retorna um **xltypeBool** contendo o código de erro passado. 
  
## <a name="example"></a>Exemplo

Este exemplo usa a função **TempErr12** para retornar um #VALUE! erro no Excel. 
  
> [!NOTE]
> A função de biblioteca da estrutura **TempErr12** aloca memória de um buffer interno, que normalmente é liberado quando a função de estrutura **Excel12f** é chamada. Se esta função de exemplo for chamada repetidamente sem o **Excel12f** ser chamado, ocorrerá um vazamento de memória. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

