---
title: Ação de macro PararMacro (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Você pode usar a ação PararMacro para interromper a macro em execução no momento.
ms.openlocfilehash: 8b80422a297647d556fb4b20cc15fb93e8853466
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429492"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>Ação de macro PararMacro (aplicativo Web personalizado do Access)

Você pode usar a **ação PararMacro** para interromper a macro em execução no momento. 
  
> [!IMPORTANT]
> A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A **ação StopMacro** não tem argumentos. 
  
## <a name="remarks"></a>Comentários

Normalmente, você usa essa ação quando uma condição torna necessário parar a macro. Por exemplo, você pode criar uma macro de interface do usuário (UI) que abre um modo de exibição mostrando os totais de ordem diária para a data inserida no modo de exibição atual. Você pode usar uma expressão condicional para garantir que o controle Data do Pedido na caixa de diálogo contenha uma data válida. Se isso não for o caso, a **ação MessageBox** poderá exibir uma mensagem de erro e a ação **PararMacro** poderá interromper a macro da interface do usuário. 
  

