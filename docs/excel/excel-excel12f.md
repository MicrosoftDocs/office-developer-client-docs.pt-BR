---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- função excel [excel 2007],função Excel12f [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431670"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Funções de biblioteca de estrutura. **O Excel** é um wrapper para a [função Excel4.](excel4-excel12.md) **Excel12f** é um wrapper para a [função Excel12.](excel4-excel12.md) Cada verificação para ver se nenhum dos argumentos é zero, o que indica que a criação de um **XLOPER ou** **XLOPER12 temporário** falhou. Se ocorrer um erro, cada uma imprimirá uma mensagem de depuração. Ao terminar, cada uma libera toda a memória temporária que pode ter sido criada para **XLOPER** e **XLOPER12** s temporários.
  
 **O Excel12f** só pode ser chamado de uma DLL a partir da biblioteca da API C do Excel 2007. Além disso, ele só funciona ao executar a partir do Excel 2007 e falha com **xlretFailed** caso contrário. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parâmetros

 _iFunction_ (**int**)
  
Um número que indica o comando ou a função que você deseja chamar. Para obter mais informações, [consulte Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Um ponteiro para o resultado da função avaliada. Qualquer memória apontada no resultado será alocada pelo Excel e deverá ser liberada em uma chamada para [xlFree](xlfree.md) assim que não for mais necessária, ou configurando **xlbitXLFree** se a retornar ao Excel. 
  
 _iCount_ (**int**)
  
O número de argumentos que serão passados para a função. A partir do Excel 2007, o limite é de 255 argumentos. Em versões anteriores, o limite é 30.
  
 _argumento1, ..._
  
Os argumentos opcionais para a função. Todos os argumentos devem ser ponteiros para **XLOPER** s no caso do **Excel** ou **XLOPER12** s no caso de **Excel12f**.
  
## <a name="return-value"></a>Valor de retorno

Ambas as funções retornam os mesmos códigos de erro e sucesso que **Excel4**, **Excel4v**, **Excel12** e **Excel12v**. Consulte [Excel4/Excel12 para](excel4-excel12.md) ver uma descrição completa desses códigos. Além disso, essas funções framework retornarão **xlretFailed** sem chamar a API de C se um ponteiro NULL para um parâmetro for detectado. 
  
## <a name="example"></a>Exemplo

Este exemplo passa um argumento ruim para a **função Excel12f,** que envia uma mensagem para o depurador. 
  
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

