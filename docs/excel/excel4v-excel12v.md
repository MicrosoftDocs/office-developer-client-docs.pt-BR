---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- função Excel12v [Excel 2007], função Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11ab86a95dde2ad52840822b28ce4d74dd05d148
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414988"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função de planilha interna do Microsoft Excel, comando ou comando de folha de macro, ou apenas função especial ou comando de XLL, de dentro de uma DLL, XLL ou recurso de código.
  
Todas as versões recentes do Excel dão suporte a **Excel4v**. A partir do Excel 2007, há suporte para **Excel12v** . 
  
Essas funções podem ser chamadas somente quando o Excel tiver passado controle para a DLL ou XLL. Eles também podem ser chamados quando o Excel tiver passado controle indiretamente por meio de uma chamada para Visual Basic for Applications (VBA). Eles não podem ser chamados em nenhum outro momento. Por exemplo, eles não podem ser chamados durante chamadas para a função DllMain ou outras vezes quando o sistema operacional chamou a DLL ou de um thread criado pela DLL. 
  
As funções [Excel4 e Excel12](excel4-excel12.md) aceitam seus argumentos como uma lista de comprimento variável na pilha, enquanto as funções **Excel4v** e **Excel12v** aceitam seus argumentos como uma matriz. Em todos os outros aspectos, o **Excel4** comporta o mesmo que **Excel4v**e **Excel12** se comporta da mesma forma que **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Parâmetros

 _iFunction_ (**int**)
  
Um número que indica o comando, a função ou a função especial que você deseja chamar. Para obter uma lista de valores de _iFunction_ válidos, consulte a seção comentários a seguir. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Um ponteiro para um **XLOPER** (no caso de **Excel4v**) ou um **XLOPER12** (no caso de **Excel12v**) que armazenará o resultado da função avaliada.
  
 _iCount_ (**int**)
  
O número de argumentos subsequentes que serão passados para a função. Em versões do Excel até 2003, pode ser qualquer número de 0 a 30. A partir do Excel 2007, pode ser qualquer número de 0 a 255.
  
 _RGX_ (**LPXLOPER []** ou **LPXLOPER12 []**)
  
Uma matriz que contém os argumentos para a função. Todos os argumentos na matriz devem ser ponteiros para valores **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valor de retorno

Essas funções retornam os mesmos valores que **Excel4** e **Excel12**.
  
## <a name="remarks"></a>Comentários

Essas funções são úteis onde o número de argumentos passados para o operador é variável. Por exemplo, **Excel4v** e **Excel12v** são úteis quando você registra funções usando o [xlfRegister](xlfregister-form-1.md) onde o número total de argumentos depende do número de argumentos feitos pela função que está sendo registrada. **Excel4v** e **Excel12v** também são úteis quando você escreve uma função de invólucro para **Excel4** ou **Excel12**. Nesses casos, você precisa converter uma lista de argumentos de variável, como seria normalmente fornecido para **Excel4** ou **Excel12**, para um único argumento de matriz de tamanho de variável para chamar de volta para o Excel usando o **Excel4v** ou o **Excel12v**.
  
### <a name="example"></a>Exemplo

Para obter exemplos de código, consulte o código para as funções do **Excel** e do **Excel12f** no Excel 2010 XLL SDK, no seguinte local onde você instalou o SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Confira também



[Excel4/Excel12](excel4-excel12.md)

