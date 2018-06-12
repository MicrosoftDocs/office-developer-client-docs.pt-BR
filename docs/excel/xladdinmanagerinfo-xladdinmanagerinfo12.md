---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- função xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765442"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamado pelo Microsoft Excel quando o Gerenciador de suplementos é invocado pela primeira vez em uma sessão do Excel. Essa função é usada para fornecer o Gerenciador de suplementos com informações sobre o add-in.
  
Excel 2007 e versões posteriores chamar **xlAddInManagerInfo12** em preferência **xlAddInManagerInfo** se exportá-los por XLL. A função **xlAddInManagerInfo12** deve funcionar da mesma maneira como **xlAddInManagerInfo** para evitar específicos da versão diferenças no comportamento da XLL. Excel espera **xlAddInManagerInfo12** para retornar um tipo de dados **XLOPER12** , enquanto **xlAddInManagerInfo** deve retornar **XLOPER**.
  
A função **xlAddInManagerInfo12** não é chamada por versões anteriores ao Excel 2007, do Excel, conforme eles não suportam o **XLOPER12**.
  
Excel não exige um XLL implementar e exportar qualquer uma dessas funções.
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>Par�metros

 _pxAction:_ Um ponteiro para um de numéricos **XLOPER/XLOPER12** (**xltypeInt** ou **xltypeNum**).
  
As informações que solicita Excel.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Se _pxAction_ for, ou pode ser forçados para, o número 1, a implementação dessa função deve retornar uma cadeia de caracteres que contém algumas informações sobre o suplemento, geralmente seu nome e talvez um número de versão. Caso contrário, ele deverá retornar #VALUE!. 
  
Se você não retornar uma cadeia de caracteres, o Excel tenta converter o valor retornado para uma cadeia de caracteres.
  
## <a name="remarks"></a>Coment�rios

Se a cadeia de caracteres retornada aponta para o buffer alocado dinamicamente, você deve garantir que esse buffer eventualmente é liberado. Se a cadeia de caracteres foi alocada pelo Excel, você pode fazer isso, definindo **xlbitXLFree**. Se a cadeia de caracteres foi alocada pela DLL, para fazer isso, a configuração **xlbitDLLFree**e você também deve implementar no [xlAutoFree](xlautofree-xlautofree12.md) (se você estiver retornando um **XLOPER**) ou **xlAutoFree12** (se você estiver retornando **XLOPER12**).
  
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



[Gerenciador de suplemento e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)

