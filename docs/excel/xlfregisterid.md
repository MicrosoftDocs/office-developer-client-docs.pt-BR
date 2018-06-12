---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- função xlfregisterid [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765478"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado a partir de uma DLL que o próprio foi chamada pelo Microsoft Excel. Se uma função já estiver registrada, ele retornará a identificação de registro existente para essa função sem registrando novamente a ele. Se uma função ainda não estiver registrada, ele registra a ele e retorna o ID do registro resultante.
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>Par�metros

_pxModuleText_ (**xltypeStr**)
  
O nome da DLL que contém a função.
  
_pxProcedure_ (**xltypeStr** ou **xltypeNum**)
  
Se uma cadeia de caracteres, o nome da função a ser chamada. Se um número, o número ordinal exportar o número da função a ser chamada. Para manter a clareza e robustez, sempre use o formulário de cadeia de caracteres.
  
_pxTypeText_ (**xltypeStr**)
  
Uma cadeia de caracteres opcional especificando os tipos de todos os argumentos para a função e o tipo do valor de retorno da função. Para obter mais informações, consulte a seção "Comentários". Este argumento pode ser emitido para um autônomo DLL (XLL) definindo **xlAutoRegister**.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Retorna a ID de registro da função (**xltypeNum**), que pode ser usada em chamadas subsequentes para **xlfUnregister**.
  
## <a name="remarks"></a>Coment�rios

Essa função é útil quando você não quiser preocupar mantendo um identificador de registro, mas você precisa de um posteriormente para cancelar o registro. Também é útil para atribuição a botões, ferramentas e menus quando a função que você deseja atribuir estiver em uma DLL.
  
Onde uma função DLL ou XLL foi registrada com um argumento válido _pxFunctionText_ tendo sido fornecido ao **xlfRegister**, sua identificação register também pode ser obtida ao passar o _pxFunctionText_ para a função **xlfEvaluate**.
  
## <a name="see-also"></a>Confira também

- [REGISTRAR](xlfregister-form-1.md)
- [CANCELAR O REGISTRO](xlfunregister-form-1.md)
- [Funções de XLM API C essenciais e úteis](essential-and-useful-c-api-xlm-functions.md)

