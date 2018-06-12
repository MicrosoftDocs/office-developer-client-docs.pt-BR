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
- função Excel12v [excel 2007], função Excel4v [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765374"
---
# <a name="excel4vexcel12v"></a>Excel4v/Excel12v

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chama uma função de planilha do Microsoft Excel interna, função de folha de macro ou comando, ou somente XLL função especial ou comando, a partir de dentro de uma DLL, XLL ou recurso de código.
  
Suportam a todas as versões recentes do Excel **Excel4v**. Iniciando no Excel 2007, **Excel12v** é suportado. 
  
Essas funções podem ser chamadas apenas quando o Excel tiver passado o controle para a DLL ou XLL. Também pode ser chamados quando o Excel passou controle indiretamente por meio de uma chamada para o Visual Basic for Applications (VBA). Eles não podem ser chamados em qualquer outro momento. Por exemplo, não pode ser chamados durante as chamadas para a função DllMain ou outros horários, quando o sistema operacional tem chamado a DLL ou de um thread criado pela DLL. 
  
As funções do [Excel4 e Excel12](excel4-excel12.md) aceitam seus argumentos como uma lista de comprimento variável na pilha, enquanto as funções **Excel4v** e **Excel12v** aceitam seus argumentos como uma matriz. Em todos os outros aspectos, **Excel4** se comporta igual **Excel4v**e **Excel12** se comporta igual **Excel12v**.
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a>Par�metros

 _iFunction_ (**int**)
  
Um número que indica o comando, função ou função especial que você deseja chamar. Para obter uma lista de valores válidos _iFunction_ , consulte a seção de comentários a seguir. 
  
 _pxRes_ (**LPXLOPER** ou **LPXLOPER12**)
  
Um ponteiro para uma **XLOPER** (no caso de **Excel4v**) ou uma **XLOPER12** (no caso de **Excel12v**) que irá armazenar o resultado da função avaliado.
  
 _iCount_ (**int**)
  
O número de argumentos subsequentes que serão passados para a função. Em versões do Excel até 2003 pode ser qualquer número entre 0 e 30. Iniciando no Excel 2007, isso pode ser qualquer número de 0 a 255.
  
 _rgx_ (**[De LPXLOPER]** ou **[] de LPXLOPER12**)
  
Uma matriz que contém os argumentos para a função. Todos os argumentos na matriz devem ser ponteiros para valores **XLOPER** ou **XLOPER12** . 
  
## <a name="return-value"></a>Valor retornado

Essas funções retornam os mesmos valores **Excel4** e **Excel12**.
  
## <a name="remarks"></a>Coment�rios

Essas funções são úteis onde o número de argumentos passados para o operador é a variável. Por exemplo, **Excel4v** e **Excel12v** são úteis quando você registra funções usando [xlfRegister](xlfregister-form-1.md) onde o número de argumentos total depende do número de argumentos tomada pela função está sendo registrada. **Excel4v** e **Excel12v** também são úteis quando você escrever uma função de wrapper para **Excel4** ou **Excel12**. Nesses casos, você precisa converter uma lista de argumentos variável, como normalmente seria ser fornecidos ao **Excel4** ou **Excel12**, como um argumento de matriz único de tamanho variável para a chamada de retorno no Excel usando **Excel4v** ou **Excel12v**.
  
### <a name="example"></a>Example

Para obter exemplos de código, consulte o código para as funções do **Excel** e **Excel12f** no SDK do Excel 2010 XLL, no seguinte local onde você instalou o SDK: 
  
Samples\Framewrk\Framewrk.c
  
## <a name="see-also"></a>Confira também



[Excel4/Excel12](excel4-excel12.md)

