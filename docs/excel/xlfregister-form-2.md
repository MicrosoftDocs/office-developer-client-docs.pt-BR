---
title: xlfRegister (formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- função xlfRegister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765465"
---
# <a name="xlfregister-form-2"></a>xlfRegister (formulário 2)

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado a partir de um comando DLL ou XLL próprio foi chamado pelo Microsoft Excel. Isso é equivalente a chamar **registrar** a partir de uma folha de macro do Excel XLM. 
  
A função **xlfRegister** pode ser chamada de duas formas: 
  
- [xlfRegister (formulário 1)](xlfregister-form-1.md): registra um comando individual ou uma função.
    
- xlfRegister (formulário 2): cargas e ativa um XLL.
    
Chamado no formulário 2, essa função pode ser usada apenas para carregar e ativar um XLL contendo um procedimento [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Par�metros

 _pxModuleText_ (**xltypeStr**)
  
O nome da DLL seja carregado e ativado.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

Se tiver êxito, isso retorna o nome da DLL (**xltypeStr**). Caso contrário, ele retornará um #VALUE! erro.
  
## <a name="see-also"></a>Confira também



[Funções de XLM API C essenciais e úteis](essential-and-useful-c-api-xlm-functions.md)

