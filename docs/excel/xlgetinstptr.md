---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765486"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o identificador de instância da instância do Microsoft Excel que atualmente está chamando uma DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parâmetros

Essa função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O identificador de instância (**xltypeBigData**) será no campo **val.bigdata.h.hdata** . 
  
## <a name="remarks"></a>Comentários

Esta função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.
  
Essa função retornará um valor correto com versões de 32 bits e 64 bits do Excel. Ele foi introduzido no Excel 2010 como uma extensão para a função de [xlGetInst](xlgetinst.md) , que funciona corretamente apenas com as versões de 32 bits do Excel. 
  
Essa função funciona corretamente quando ele é chamado usando as variedades [Excel4 e Excel12](excel4-excel12.md) das funções de retorno de chamada de API, porque **XLOPER** e **XLOPER12** tem a mesma estrutura que suporta o valor de **xltypeBigData** Digite. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir compara a instância da última cópia do Excel que a chamou com a cópia atual do Excel que a chamou. Se eles forem iguais, ele retornará 1; Caso contrário, retornará 0; Se a função falhar, ele retornará -1. Este exemplo funciona com versões de 32 bits e 64 bits do Excel.
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>Confira também

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

