---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- Função xlgetinst [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e113ddbf55e2b4651d578549802c44e2c6413a18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428127"
---
# <a name="xlgetinst"></a>xlGetInst

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Retorna o alça de instância da instância do Microsoft Excel que está chamando uma DLL no momento.
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>Parâmetros

Esta função não tem argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O alça de instância (**xltypeInt**) estará no **campo val.w.** 
  
## <a name="remarks"></a>Comentários

Essa função pode ser usada para distinguir entre várias instâncias em execução do Excel que estão chamando a DLL.
  
Quando você está chamando essa função usando [Excel4](excel4-excel12.md) ou [Excel4v](excel4v-excel12v.md), a variável de inteiro XLOPER retornada é um int de 16 bits curto assinado. Isso só é capaz de conter os 16 bits baixos do alça do Windows de 32 bits. A partir do Excel 2007, a variável inteira do **XLOPER12** é um int de 32 bits assinado e, portanto, contém o alça inteira, removendo a necessidade de iterar todas as janelas abertas. 
  
> [!IMPORTANT]
> Se a **função xlGetInst** for usada com a versão de 64 bits do Microsoft Excel, a função falhará. Isso ocorre porque o tipo **de valor xltypeInt** não é largo o suficiente para manter a alça longa de 64 bits retornada pelo Excel nesse caso. Para essa finalidade, o Excel 2010 introduziu uma nova função chamada [xlGetInstPtr](xlgetinstptr.md), que é executado corretamente com as versões de 32 bits e 64 bits do Excel. 
  
## <a name="example"></a>Exemplo

O exemplo a seguir compara a instância da última cópia do Excel que a chamou à cópia atual do Excel que a chamou. Se eles são iguais, retornará 1; caso não seja, retornará 0; se a função falhar, retornará -1.
  
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

