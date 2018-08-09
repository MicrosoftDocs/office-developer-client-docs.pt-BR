---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- função xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765474"
---
# <a name="xlgetinst"></a>xlGetInst

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o identificador de instância da instância do Microsoft Excel que atualmente está chamando uma DLL.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parâmetros

Essa função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O identificador de instância (**xltypeInt**) será no campo **val.w** . 
  
## <a name="remarks"></a>Comentários

Esta função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.
  
Quando você chama essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um curto int 16 bits assinado, a. Isso só é capaz de conter os 16 bits baixos da alça de Windows de 32 bits. Iniciando no Excel 2007, a variável de inteiro de **XLOPER12** é um int assinado de 32 bits e, portanto, contém um manipulador de inteiro, removendo a necessidade de iterar todas as janelas abertas. 
  
> [!IMPORTANT]
> Se a função **xlGetInst** é usada com a versão de 64 bits do Microsoft Excel, a função falhará. Isso ocorre porque o tipo de valor **xltypeInt** não é ampla o suficiente para armazenar a alça de 64 bits longa retornada pelo Excel neste caso. Para esse fim, o Excel 2010 introduziu uma nova função chamada [xlGetInstPtr](xlgetinstptr.md), que é executado corretamente com as versões 32 bits e 64 bits do Excel. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir compara a instância da última cópia do Excel que a chamou com a cópia atual do Excel que a chamou. Se eles forem iguais, ele retornará 1; Caso contrário, retornará 0; Se a função falhar, ele retornará -1.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
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



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

