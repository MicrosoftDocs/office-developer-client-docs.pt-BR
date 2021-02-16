---
title: xlfUnregister (Formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419902"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (Formulário 2)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel. Isso equivale a chamar **UNREGISTER de** uma folha de macro XLM do Excel. 
  
**xlfUnregister** pode ser chamado de duas formas: 
  
- Formulário 1: Desastra o registro de um comando ou função individual.
    
- Formulário 2: Descarrega e desativa um XLL.
    
Chamada no Formulário 2, essa função força um DLL ou recurso de código a ser descarregado completamente. Ele desastra o registro de todas as funções em uma DLL, mesmo se elas estão sendo usadas por outra macro, independentemente da contagem de uso. Essa função chama **xlAutoClose** e, em seguida, desautorna todas as funções na DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parâmetros

_pxModuleText_ (**xltypeStr**)
  
O nome da DLL.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se bem-sucedido, **retorna VERDADEIRO** (**xltypeBool**). Se não tiver êxito, **retornará FALSE**.
  
## <a name="remarks"></a>Comentários

> [!NOTE] 
> Não chame essa forma da função de sua implementação do [xlAutoClose](xlautoclose.md) em uma tentativa de ressumentar todos os recursos da DLL com uma chamada de função simples. Isso leva à chamada recursiva **de xlAutoClose** e a um estouro de pilha. 
  
### <a name="remember-to-delete-names"></a>Lembre-se de excluir nomes

Se você especificou o argumento  _pxFunctionText_ para **xlfRegister**, ao registrar as funções e comandos da DLL, exclua explicitamente os nomes chamando **xlfSetName** para cada um deles, omitindo o segundo argumento para que a função não apareça mais no Assistente de Função. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Confira também

- [xlfRegister (Formulário 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formulário 1)](xlfunregister-form-1.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

