---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fd4b4ad5bf52f29384ef7e0ba738c350189f471e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310049"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o identificador de instância da instância do Microsoft Excel que está atualmente chamando uma DLL.
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parâmetros

Esta função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O identificador de instância (**xltypeBigData**) será no campo **Val. bigdata. h. hData** . 
  
## <a name="remarks"></a>Comentários

Essa função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.
  
Essa função retorna um valor correto com as versões de 32 bits e 64 bits do Excel. Ele foi introduzido no Excel 2010 como uma extensão para a função [xlGetInst](xlgetinst.md) , que funciona corretamente apenas com as versões de 32 bits do Excel. 
  
Essa função funciona corretamente quando é chamada usando o [Excel4 e o Excel12](excel4-excel12.md) variedades das funções de retorno de chamada da API, porque **XLOPER** e **XLOPER12** têm a mesma estrutura que dá suporte ao valor **xltypeBigData** Escreva. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir compara a instância da última cópia do Excel que a chamou para a cópia atual do Excel que a chamou. Se forem iguais, retornará 1; caso contrário, retornará 0; se a função falhar, ela retornará-1. Este exemplo funciona com as versões de 32 bits e 64 bits do Excel.
  
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

