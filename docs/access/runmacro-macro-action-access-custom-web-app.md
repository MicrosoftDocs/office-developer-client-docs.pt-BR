---
title: Ação de macro ExecutarMacro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 59ba365d-cff5-4126-bc22-4d5a37578aab
description: Você pode usar a ação RunMacro para executar uma macro de interface do usuário (UI).
ms.openlocfilehash: 98e3b17a6c64fa12ac37e4551d45714c873f5ccb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438439"
---
# <a name="runmacro-macro-action-access-custom-web-app"></a>Ação de macro ExecutarMacro (aplicativo Web personalizado do Access)

Você pode usar a **ação RunMacro** para executar uma macro de interface do usuário (UI). 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **ExecutarMacro** tem os argumentos a seguir. 
  
|**Argumento da ação**|**Descrição**|
|:-----|:-----|
|**Macro Name** <br/> |O nome da macro de interface do usuário a ser executado.  <br/> |
   
## <a name="remarks"></a>Comentários

Quando você executa uma macro de interface do usuário que contém a ação **ExecutarMacro** e ela atinge a ação **ExecutarMacro,** o Access executa a macro de interface do usuário chamada. Quando a macro da interface do usuário chamada tiver sido concluída, o Access retornará à macro de interface do usuário original e executa a próxima ação. 
  

