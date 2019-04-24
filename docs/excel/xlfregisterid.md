---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- função xlfregisterid [Excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 05119226d0b6190a2c4b30846c03a59b5c3cd1d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303875"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado a partir de uma DLL que tenha sido chamada pelo Microsoft Excel. Se uma função já estiver registrada, retornará a ID de registro existente para essa função sem registrá-la novamente. Se uma função ainda não estiver registrada, ela a registrará e retornará a ID de registro resultante.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Parâmetros

_pxModuleText_ (**xltypeStr**)
  
O nome da DLL que contém a função.
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Se uma cadeia de caracteres, o nome da função a ser chamada. Se número, o número de exportação ordinal da função a chamar. Para claridade e robustez, sempre use o formulário de cadeia de caracteres.
  
_pxTypeText_ (**xltypeStr**)
  
Uma cadeia de caracteres opcional que especifica os tipos de todos os argumentos para a função e o tipo do valor de retorno da função. Para obter mais informações, consulte a seção "Comentários". Esse argumento pode ser omitido para uma DLL autônoma (XLL) definindo **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Retorna a ID de registro da função (**xltypeNum**), que pode ser usada em chamadas subsequentes para **xlfUnregister**.
  
## <a name="remarks"></a>Comentários

Essa função é útil quando você não deseja se preocupar em manter uma ID de registro, mas precisa de uma posteriormente para cancelar o registro. Também é útil para atribuir menus, ferramentas e botões quando a função que você deseja atribuir está em uma DLL.
  
Onde uma função DLL ou XLL foi registrada com um argumento _pxFunctionText_ válido tendo sido fornecida ao **XLFREGISTER**, sua ID de registro também pode ser obtida passando o _pxFunctionText_ para a função **xlfEvaluate**.
  
## <a name="see-also"></a>Confira também

- [REMOVER](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

