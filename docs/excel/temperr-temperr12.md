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
- função temperr [excel 2007], função TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765435"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de Framework que cria um temporário **XLOPER**/ **XLOPER12** contendo um erro de planilha do Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Par�metros

 _Err_
  
O código de erro desejado ou seu equivalente numérico literal, conforme mostrado na tabela a seguir.
  
|**Erro**|**Código de erro definido no XLCALL. H**|**Equivalente decimal**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Valor retornado

Retorna um **xltypeBool** que contém o código de erro passados. 
  
## <a name="example"></a>Example

Este exemplo usa a função **TempErr12** para retornar um #VALUE! erro para o Excel. 
  
> [!NOTE]
> A função de biblioteca Framework **TempErr12** aloca memória de um buffer interno, que normalmente é liberado quando a função Framework **Excel12f** é chamada. Se a função neste exemplo é chamada repetidamente sem **Excel12f** está sendo chamado, ocorre um vazamento de memória. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

