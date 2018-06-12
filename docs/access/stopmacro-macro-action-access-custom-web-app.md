---
title: Ação de Macro PararMacro (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: af28534b-6f0d-43ee-ae89-ee2f85da1af1
description: Você pode usar a ação PararMacro para interromper a macro em execução no momento.
ms.openlocfilehash: 54501b65eb1847287e810ae43742a2e6e5384264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765229"
---
# <a name="stopmacro-macro-action-access-custom-web-app"></a>Ação de Macro PararMacro (aplicativo da web personalizado do Access)

Você pode usar a ação **PararMacro** para interromper a macro em execução no momento. 
  
> [!IMPORTANT]
> [!IMPORTANTE] A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis. 
  
## <a name="setting"></a>Configuração

A ação **PararMacro** não tem nenhum argumento. 
  
## <a name="remarks"></a>Coment�rios

Geralmente você usa esta ação quando uma condição torna necessário para interromper a macro. Por exemplo, você pode criar uma macro (UI) da interface de usuário que abre uma exibição mostrando os totais de ordem de diário para a data inserida na exibição atual. Você poderia usar uma expressão condicional para certificar-se de que o controle de data do pedido na caixa de diálogo contém uma data válida. Caso contrário, a ação **MessageBox** pode exibir uma mensagem de erro e a ação **PararMacro** pode interromper a macro de interface do usuário. 
  

