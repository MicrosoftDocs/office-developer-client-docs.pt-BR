---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- função xlstack [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 55ceed93407b1d99e05bc20fb6ce0b22459de7df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429976"
---
# <a name="xlstack"></a>xlStack

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Verifica a quantidade de espaço que resta na pilha.
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna o número de bytes (**xltypeInt**) restantes na pilha.
  
## <a name="remarks"></a>Comentários

A quantidade de espaço em pilha disponível de versões recentes excedentes ao inteiro assinado de 16 bits do **XLOPER**. Isso significa que **xlStack** pode retornar um valor entre -32767 e 32768 quando chamado usando **XLOPER** s e **Excel4** ou **Excel4v**. Para obter o valor correto nesse caso, você deve lançar o valor retornado para um curto não assinado.
  
A partir do Excel 2007, você deve chamar essa função usando **XLOPER12** s e **Excel12** ou **Excel12v**, nesse caso, o valor retornado é a quantidade de espaço em pilha disponível ou 64 KB, o que for menor.
  
O Excel tem uma quantidade limitada de espaço na pilha, e você deve ter cuidado para não sobrecarr o espaço. Nunca coloque estruturas de dados muito grandes na pilha e faça o máximo possível de variáveis locais estáticas. Evite chamar funções recursivamente, pois isso preencherá rapidamente a pilha.
  
Se você suspeitar que está anulando a pilha, chame essa função com frequência para ver quanto espaço na pilha é deixado.
  
## <a name="example"></a>Exemplo

O primeiro exemplo exibe uma mensagem de alerta contendo a quantidade de espaço em pilha à esquerda e está contida em  `\SAMPLES\EXAMPLE\EXAMPLE.C` . O segundo exemplo faz a mesma coisa, trabalhando com **XLOPER** s e não está contido no código de exemplo do SDK.
  
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

