---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- função xlAutoRegister [Excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f043558f3f642001e9ba11ee5b18a2721c3dddfb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421162"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
O Excel chama a [função xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada foi feita ao registrador **** de função XLM ou à [função xlfRegister](xlfregister-form-1.md)equivalente da API C, com os tipos de argumento e de retorno da função que está sendo registrada ausente. Permite que o XLL pesquise suas listas internas de funções e comandos exportados para registrar a função com os tipos de argumento e de retorno especificados.
  
A partir do Excel 2007, o Excel chama a função **xlAutoRegister12** em preferência para a função **xlAutoRegister** se ela for exportada pelo XLL. 
  
O Excel não requer que um XLL implemente e exporte uma dessas funções.
  
> [!NOTE]
> Se **xlAutoRegister**/ **xlAutoRegister12** tentar registrar a função sem fornecer os tipos de argumento e de retorno, ocorrerá um loop de chamada recursiva, que eventualmente estourará a pilha de chamadas e travará o Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parâmetros

 _pxName_ (**xltypeStr**)
  
O nome da função XLL que está sendo registrada.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função deve retornar o resultado da tentativa de registrar a função XLL _pxName_ usando a função **xlfRegister** . Se a função especificada não for uma das exportações do XLL, ela deverá retornar o **#VALUE!** erro ou **nulo** que o Excel irá interpretar em **#VALUE!**.
  
## <a name="remarks"></a>Comentários

Sua implementação do **xlAutoRegister** deve realizar uma pesquisa que não diferencia maiúsculas de minúsculas nas listas internas de funções e comandos que ele exporta procurando por uma correspondência com o nome aprovado. Se a função ou o comando for encontrado, **xlAutoRegister** deve tentar registrá-lo, usando a função **xlfRegister** , certificando-se de fornecer a cadeia de caracteres que informa ao Excel os tipos de argumento e de retorno da função, bem como qualquer outro necessário informações sobre a função. Em seguida, ele deve retornar ao Excel, qualquer que seja a chamada para **xlfRegister** retornada. Se a função foi registrada com êxito, **xlfRegister** retorna um valor **xltypeNum** que contém a ID de registro da função. 
  
### <a name="example"></a>Exemplo

ConFira o `SAMPLES\EXAMPLE\EXAMPLE.C` arquivo para obter um exemplo de implementação dessa função. 
  
## <a name="see-also"></a>Confira também



[REMOVER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

