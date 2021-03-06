---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Função xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407792"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel quando o Gerenciador de Complementos é invocado pela primeira vez em uma sessão do Excel. Essa função é usada para fornecer ao Add-In Do usuário informações sobre o seu complemento.
  
O Excel 2007 e versões posteriores chamam **xlAddInManagerInfo12** de preferência para **xlAddInManagerInfo** se exportado pelo XLL. A **função xlAddInManagerInfo12** deve funcionar da mesma maneira que **xlAddInManagerInfo** para evitar diferenças específicas de versão no comportamento do XLL. O Excel espera **que xlAddInManagerInfo12** retorne um tipo de dados **XLOPER12,** enquanto **xlAddInManagerInfo** deve retornar um **XLOPER**.
  
A **função xlAddInManagerInfo12** não é chamada por versões do Excel anteriores ao Excel 2007, pois elas não têm suporte para **XLOPER12**.
  
O Excel não exige um XLL para implementar e exportar qualquer uma dessas funções.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Parâmetros

 _pxAction:_ Um ponteiro para um **XLOPER/XLOPER12** numérico (**xltypeInt** ou **xltypeNum**).
  
As informações que o Excel está solicitando.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se  _pxAction_ for ou puder ser coerced para o número 1, sua implementação dessa função deverá retornar uma cadeia de caracteres contendo algumas informações sobre o complemento, normalmente seu nome e talvez um número de versão. Caso contrário, ele deve retornar #VALUE!. 
  
Se você não retornar uma cadeia de caracteres, o Excel tentará converter o valor retornado em uma cadeia de caracteres.
  
## <a name="remarks"></a>Comentários

Se a cadeia de caracteres retornada aponta para buffer alocado dinamicamente, você deve garantir que esse buffer seja liberado eventualmente. Se a cadeia de caracteres foi alocada pelo Excel, faça isso definindo **xlbitXLFree**. Se a cadeia de caracteres foi alocada pela DLL, você faz isso definindo **xlbitDLLFree** e também deve implementar em [xlAutoFree](xlautofree-xlautofree12.md) (se você estiver retornando um **XLOPER**) ou **xlAutoFree12** (se estiver retornando um **XLOPER12**).
  
## <a name="example"></a>Exemplo

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>Confira também



[Gerenciador de Suplemento e Funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

