---
title: Implementar uma interface de configuração para provedores de repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332974"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementar uma interface de configuração para provedores de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositórios de mensagens são necessários para implementar uma interface que permite que o usuário configure o provedor de repositório de mensagens para ser executado no computador desse usuário. Normalmente, o provedor do repositório de mensagens é configurado quando o provedor do repositório de mensagens é adicionado ao perfil de um usuário. A interface de configuração do provedor de repositório de mensagens geralmente trata de tarefas como configurar nomes de usuário e senhas para repositórios de mensagens protegidos, escolher caminhos para arquivos necessários e criar o mecanismo de armazenamento subjacente que ele usará, se necessário.
  
A interface de configuração implementada é acessada por pontos de entrada adicionais na DLL do provedor de serviços de mensagens. Para obter mais informações, consulte [Configuring a Message Service](configuring-a-message-service.md). A interface de configuração do provedor de repositório de mensagens é a única interface de usuário que um provedor de armazenamento de mensagens deve implementar.
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

