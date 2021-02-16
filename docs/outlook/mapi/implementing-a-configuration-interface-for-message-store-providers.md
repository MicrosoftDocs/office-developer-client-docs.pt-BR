---
title: Implementando uma interface de configuração para provedores de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c349a03b0be465ed1262712372b6ee17a9812abd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415884"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementando uma interface de configuração para provedores de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de armazenamento de mensagens são necessários para implementar uma interface que permite ao usuário configurar o provedor de armazenamento de mensagens para executar no computador desse usuário. Normalmente, o provedor de armazenamento de mensagens é configurado quando o provedor de armazenamento de mensagens é adicionado ao perfil de um usuário. A interface de configuração do provedor de armazenamento de mensagens geralmente lida com tarefas como definir nomes de usuário e senhas para armazenamentos de mensagens protegidos, escolher caminhos para os arquivos necessários e criar o mecanismo de armazenamento subjacente que ele usará, se necessário.
  
A interface de configuração implementada é acessada por meio de pontos de entrada adicionais na DLL do provedor de serviços de mensagens. Para obter mais informações, [consulte Configurando um serviço de mensagens.](configuring-a-message-service.md) A interface de configuração do provedor de armazenamento de mensagens é a única interface do usuário que um provedor de armazenamento de mensagens deve implementar.
  
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

