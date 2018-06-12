---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- função do Excel [excel 2007], função Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765301"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções da biblioteca de estrutura. **Excel** é um wrapper para a função [Excel4](excel4-excel12.md) . **Excel12f** é um wrapper para a função [Excel12](excel4-excel12.md) . Cada verifica se nenhum dos argumentos é zero, o que indicaria que a criação de um temporário **XLOPER** ou **XLOPER12** falhou. Se ocorrer um erro, cada imprime uma mensagem de depuração. Quando terminar, cada libera toda a memória temporária que possa ter sido criada para s temporário do **XLOPER**e **XLOPER12**s.
  
 **Excel12f** só pode ser chamado a partir de uma DLL começando com a biblioteca do C API do Excel 2007. Além disso, ele só funciona durante a execução começando com o Excel 2007 e falha com **xlretFailed** caso contrário. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Par�metros

 _iFunction_ (**int**)
  
Um número indicando o comando ou uma função que você deseja chamar. Para obter mais informações, consulte [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Um ponteiro para o resultado da função avaliado. Qualquer memória apontada no resultado terá sido alocada pelo Excel e deve ser liberada em uma chamada para [xlFree](xlfree.md) depois que ele não é mais necessária, ou definindo **xlbitXLFree** se retorná-lo para o Excel. 
  
 _iCount_ (**int**)
  
O número de argumentos que serão passadas para a função. Iniciando no Excel 2007, o limite é 255 argumentos. Nas versões anteriores, o limite é 30.
  
 _Argumento1,..._
  
Os argumentos opcionais para a função. Todos os argumentos devem ser ponteiros para s **XLOPER**no caso do **Excel**ou **XLOPER12**s no caso de **Excel12f**.
  
## <a name="return-value"></a>Valor retornado

Ambas as funções retornam o mesmo erro e códigos de sucesso como **Excel4**, **Excel4v**, **Excel12**e **Excel12v**. Consulte [Excel4/Excel12](excel4-excel12.md) para obter uma descrição completa desses códigos. Além disso, essas funções de Framework retornam **xlretFailed** sem chamar a API C se um ponteiro NULL a um parâmetro é detectado. 
  
## <a name="example"></a>Example

Este exemplo passa um argumento inválido para a função de **Excel12f** , que envia uma mensagem ao depurador. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Excel4/Excel12](excel4-excel12.md)


[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

