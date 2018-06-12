---
title: Funções de XLM API C essenciais e úteis
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- funções [excel 2007], xlm do c api
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765285"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a>Funções de XLM API C essenciais e úteis

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
As funções descritas nesta seção são funções de retorno de chamada do Microsoft Excel que são particularmente úteis para os desenvolvedores DLL e XLL. Desses, a função **xlfRegister** é essencial para XLLs e DLLs que deseja registrar suas funções e comandos para que eles possam ser chamados diretamente do Excel. As funções **xlfUnregister** e **xlfSetName** são usados em combinação para cancelar o registro de comandos e funções DLL e XLL. 
  
Muito mais funções são expostas pelo Excel por meio da API C que são úteis quando você estiver desenvolvendo XLLs. Elas correspondem à planilha do Excel funções e funções e comandos que estão disponíveis a partir de folhas de macro XLM.
  
## <a name="in-this-section"></a>Nesta se��o

[xlfCaller](xlfcaller.md)
  
[xlfEvaluate](xlfevaluate.md)
  
[xlfGetDef](xlfgetdef.md)
  
[xlfGetName](xlfgetname.md)
  
[xlfRegister (Form 1)](xlfregister-form-1.md)
  
[xlfRegister (formulário 2)](xlfregister-form-2.md)
  
[xlfRegisterId](xlfregisterid.md)
  
[xlfUnregister (formulário 1)](xlfunregister-form-1.md)
  
[xlfUnregister (formulário 2)](xlfunregister-form-2.md)
  
[xlfSetName](xlfsetname.md)
  

