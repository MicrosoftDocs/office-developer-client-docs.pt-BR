---
title: xlfRegister (Formulário 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- função xlfregister [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416038"
---
# <a name="xlfregister-form-2"></a>xlfRegister (Formulário 2)

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Pode ser chamado de um comando DLL ou XLL que, por sua vez, foi chamado pelo Microsoft Excel. Isso equivale a chamar **Register** de uma folha de macro XLM do Excel. 
  
A função **xlfRegister** pode ser chamada em duas formas: 
  
- [xlfRegister (formulário 1)](xlfregister-form-1.md): registra um comando ou função individual.
    
- xlfRegister (Formato 2): carrega e ativa um XLL.
    
Chamado no formato 2, essa função só pode ser usada para carregar e ativar um XLL contendo um procedimento [xlAutoOpen](xlautoopen.md) . 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parâmetros

 _pxModuleText_ (**xltypeStr**)
  
O nome da DLL a ser carregada e ativada.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Se tiver êxito, retornará o nome da DLL (**xltypeStr**). Caso contrário, retornará um #VALUE! #NUM!
  
## <a name="see-also"></a>Confira também



[Funções XLM essenciais e úteis para a API C](essential-and-useful-c-api-xlm-functions.md)

