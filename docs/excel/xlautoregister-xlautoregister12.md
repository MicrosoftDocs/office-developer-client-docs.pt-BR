---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- função xlautoregister [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19765453"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Excel chama a [função xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada foi feita para a função XLM **registrar**ou C API equivalente [xlfRegister função](xlfregister-form-1.md), com os tipos de retorno e o argumento da função que está sendo registrado ausente. Ele permite que o XLL pesquisar seus listas internas de funções exportadas e comandos para registrar a função com o argumento e retornar tipos especificados.
  
Iniciando no Excel 2007, Excel chama a função **xlAutoRegister12** em preferência a função **xlAutoRegister** se ele é exportado pelo XLL. 
  
Excel não exige um XLL implementar e exportar qualquer uma dessas funções.
  
> [!NOTE]
> Se **xlAutoRegister**/ **xlAutoRegister12** tenta registrar a função sem fornecer o argumento e tipos de retorno, um loop de chamada recursiva ocorre que eventualmente estourar a pilha de chamada e Excel de travamento. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Par�metros

 _pxName_ (**xltypeStr**)
  
O nome da função XLL que está sendo registrado.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A função deve retornar o resultado da tentativa de registrar a função XLL _pxName_ , usando a função **xlfRegister** . Se a função especificada não for uma das exportações do XLL, ele deve retornar o **#VALUE!** erro ou **Nulo** que Excel irá interpretar em **#VALUE!**.
  
## <a name="remarks"></a>Coment�rios

A implementação dos **xlAutoRegister** deve realizar uma pesquisa diferenciam maiusculas e minúsculas através de listas de interno do seu XLL das funções e comandos que ele exporta procurando uma correspondência com o nome passado. Se a função ou o comando for localizado, **xlAutoRegister** deve tentar registrar a ele, usando a função **xlfRegister** , certificando-se de fornecer a cadeia de caracteres que indica os tipos de retorno e o argumento de função, bem como qualquer outro necessários ao Excel informações sobre a função. Em seguida, ele deverá retornar para o Excel vivo do que a chamada para **xlfRegister** retornado. Se a função foi registrada com êxito, **xlfRegister** retorna um valor **xltypeNum** que contém a ID de registrar da função. 
  
### <a name="example"></a>Example

Consulte o arquivo `SAMPLES\EXAMPLE\EXAMPLE.C` para um exemplo de implementação dessa função. 
  
## <a name="see-also"></a>Confira também



[REGISTRAR](xlfregister-form-1.md)
  
[CANCELAR O REGISTRO](xlfunregister-form-1.md)

