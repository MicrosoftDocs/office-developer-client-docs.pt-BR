---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- Função xlautoregister [excel 2007]
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
  
O Excel chama a função [xlAutoRegister](xlautoregister-xlautoregister12.md) sempre que uma chamada é feita para a função XLM **REGISTER** ou a função [equivalente xlfRegister](xlfregister-form-1.md)da API C, com os tipos de retorno e argumento da função sendo registrada ausentes. Ele permite que o XLL pesquise suas listas internas de funções e comandos exportados para registrar a função com o argumento e os tipos de retorno especificados.
  
A partir do Excel 2007, o Excel chama a função **xlAutoRegister12** de preferência para a função **xlAutoRegister** se ela for exportada pelo XLL. 
  
O Excel não exige um XLL para implementar e exportar qualquer uma dessas funções.
  
> [!NOTE]
> Se **xlAutoRegister** /  **xlAutoRegister12** tentar registrar a função sem fornecer o argumento e os tipos de retorno, ocorrerá um loop de chamada recursiva que eventualmente exceda a pilha de chamada e trava o Excel. 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>Parâmetros

 _pxName_ (**xltypeStr**)
  
O nome da função XLL que está sendo registrada.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função deve retornar o resultado da tentativa de registrar a função _PXName_ XLL usando a **função xlfRegister.** Se a função especificada não for uma das exportações do XLL, ela deverá retornar o **#VALUE!** ou **NULL** que o Excel interpretará em **#VALUE!**.
  
## <a name="remarks"></a>Comentários

Sua implementação do **xlAutoRegister** deve realizar uma pesquisa que não faça maiúsculas de minúsculas nas listas internas de funções e comandos do XLL que ele exporta procurando uma combinação com o nome passado. Se a função ou o comando for encontrado, **xlAutoRegister** deverá tentar registrá-lo, usando a função **xlfRegister,** fornecendo a cadeia de caracteres que informa ao Excel os tipos de retorno e argumento da função, bem como quaisquer outras informações necessárias sobre a função. Em seguida, ele deve retornar ao Excel independentemente da chamada para **xlfRegister** retornada. Se a função tiver sido registrada com êxito, **xlfRegister** retornará um valor **xltypeNum** contendo a ID do Registro da função. 
  
### <a name="example"></a>Exemplo

Consulte o arquivo  `SAMPLES\EXAMPLE\EXAMPLE.C` para ver um exemplo de implementação dessa função. 
  
## <a name="see-also"></a>Confira também



[REGISTER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

