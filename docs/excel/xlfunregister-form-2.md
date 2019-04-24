---
title: xlfUnregister (Formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [Excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310161"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (Formulário 2)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel. Isso equivale a chamar **Unregister** de uma folha de macro XLM do Excel. 
  
**xlfUnregister** pode ser chamado de duas formas: 
  
- Formulário 1: cancela o registro de um comando ou função individual.
    
- Formulário 2: descarrega e desativa um XLL.
    
Chamado no formato 2, essa função força uma DLL ou recurso de código a ser descarregado completamente. Ele cancela o registro de todas as funções em uma DLL, mesmo que estejam atualmente em uso por outra macro, independentemente da contagem de uso. Essa função chama **xlAutoClose**e, em seguida, cancela o registro de todas as funções na dll.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parâmetros

_pxModuleText_ (**xltypeStr**)
  
O nome da DLL.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se bem-sucedido, retorna **true** (**xltypeBool**). Se não tiver êxito, retornará **false**.
  
## <a name="remarks"></a>Comentários

> [!NOTE] 
> Não chame esse formato da função de sua implementação do [xlAutoClose](xlautoclose.md) em uma tentativa de cancelar o registro de todos os recursos da dll com uma única chamada de função simples. Isso leva à chamada recursiva de **xlAutoClose** e de um estouro de pilha. 
  
### <a name="remember-to-delete-names"></a>Lembre-se de excluir nomes

Se você especificou o argumento _pxFunctionText_ como **xlfRegister**, ao registrar as funções e os comandos da dll, deverá excluir explicitamente os nomes chamando **xlfSetName** para cada um, omitindo o segundo argumento para que o a função não é mais exibida no assistente de função. Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Confira também

- [xlfRegister (Formulário 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formulário 1)](xlfunregister-form-1.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

