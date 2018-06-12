---
title: xlfUnregister (formulário 2)
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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765488"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (formulário 2)

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel. Isso é equivalente a chamar **cancela o registro** de uma folha de macro do Excel XLM. 
  
**xlfUnregister** pode ser chamado de duas formas: 
  
- Formulário 1: Cancela o registro de um comando individual ou uma função.
    
- Formulário 2: Descarrega e desativa um XLL.
    
Chamado no formulário 2, essa função força um DLL ou código do recurso a ser descarregado completamente. Ele cancela o registro de todas as funções em uma DLL, mesmo se eles estão atualmente em uso por outra macro, não importa qual a contagem de uso. Essa função chama **xlAutoClose**e, em seguida, cancela o registro de todas as funções na DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Par�metros

_pxModuleText_ (**xltypeStr**)
  
O nome da DLL.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Se tiver êxito, retornará **TRUE** (**xltypeBool**). Se for bem sucedida, retornará **FALSE**.
  
## <a name="remarks"></a>Coment�rios

> [!NOTE] 
> Não chame essa forma da função da sua implementação do [xlAutoClose](xlautoclose.md) em uma tentativa de cancelar o registro de todos os recursos da DLL com chamada de uma função simples. Isso leva a chamada recursiva de **xlAutoClose** e um estouro de pilha. 
  
### <a name="remember-to-delete-names"></a>Lembre-se de excluir nomes

Se você especificou o argumento _pxFunctionText_ de **xlfRegister**, ao registrar a DLL as funções e comandos, você deve explicitamente excluir os nomes chamando **xlfSetName** para cada um, omitindo o segundo argumento para que o função não aparece mais no Assistente de função. Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Confira também

- [xlfRegister (Form 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (formulário 1)](xlfunregister-form-1.md)
- [Funções de XLM API C essenciais e úteis](essential-and-useful-c-api-xlm-functions.md)

