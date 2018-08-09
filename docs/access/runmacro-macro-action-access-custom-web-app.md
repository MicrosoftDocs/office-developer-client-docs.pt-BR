---
title: Ação de Macro ExecutarMacro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Você pode usar a ação ExecutarMacro para executar uma macro (UI) da interface de usuário.
ms.openlocfilehash: 68a59e246c0af8385a17aedcf3da771c720f8fd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765223"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>Ação de Macro ExecutarMacro (aplicativo da web personalizado do Access)

Você pode usar a ação **ExecutarMacro** para executar uma macro (UI) da interface de usuário. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ExecutarMacro** tem os argumentos a seguir. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
|**Macro Name** <br/> |O nome da macro a interface do usuário a ser executada.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando você executar uma macro de interface do usuário que contém a ação **ExecutarMacro** e alcançar a ação **ExecutarMacro** , o Access executa a macro chamada da interface do usuário. Quando a macro chamada da interface do usuário for concluída, o Access retorna à macro da interface do usuário original e executa a próxima ação. 
  

