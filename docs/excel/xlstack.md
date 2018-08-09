---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- função xlStack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765482"
---
# <a name="xlstack"></a>xlStack

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Verifica a quantidade de espaço deixado na pilha.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna o número de bytes (**xltypeInt**) restante na pilha.
  
## <a name="remarks"></a>Comentários

A quantidade de espaço de pilha disponível das versões recentes estouros de inteiro assinado de 16 bits de **XLOPER**. Isso significa que **xlStack** pode retornar um valor entre-32767 e 32768 quando chamado usando **XLOPER**s e **Excel4** ou **Excel4v**. Para obter o valor correto, nesse caso, você deve converter o valor retornado para um unsigned short.
  
Iniciando no Excel 2007, você deve chamar essa função usando **XLOPER12**s e **Excel12** ou **Excel12v**, caso em que o valor retornado será a quantidade de espaço em pilha disponível ou de 64 KB, o que for o menor.
  
O Excel tem uma quantidade de espaço limitada na pilha e você deve ter cuidado para não saturação esse espaço. Nunca colocado estruturas de dados muito grande na pilha e faça como muitas variáveis locais quanto possível estático. Evite chamando funções recursivamente, porque o que será preenchido rapidamente a pilha de itens.
  
Se você achar que você está saturar a pilha, chame essa função com frequência para ver quanto espaço em pilha é da esquerda.
  
## <a name="example"></a>Exemplo

O primeiro exemplo exibe uma mensagem de alerta contendo a quantidade de espaço de pilha deixado e está contido no `\SAMPLES\EXAMPLE\EXAMPLE.C`. O segundo exemplo faz a mesma coisa, trabalhando com **XLOPER**s e não está contido no código de exemplo do SDK.
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>Confira também

- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

