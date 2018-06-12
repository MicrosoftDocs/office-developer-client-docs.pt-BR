---
title: Implementando uma Interface de configuração para provedores de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 508e6950-d483-4cbe-b817-8016f4aa5cd8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f7151841eef180a78a13ad161d197af783decfb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767385"
---
# <a name="implementing-a-configuration-interface-for-message-store-providers"></a>Implementando uma Interface de configuração para provedores de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 
  
Provedores de armazenamento de mensagem são necessários para implementar uma interface que permite ao usuário configurar o provedor de armazenamento de mensagens para ser executado no computador do usuário. Normalmente, o provedor de armazenamento de mensagens é configurado quando o provedor de armazenamento de mensagem é adicionado a um perfil de usuário. Interface de configuração do provedor de repositório a mensagem geralmente trata de tarefas, como a definição de nomes de usuário e senhas para repositórios de mensagem protegida, escolhendo caminhos para os arquivos necessários, e criando o mecanismo de armazenamento subjacente ele usará, se necessário.
  
Você implementar a interface de configuração é acessada através de pontos de entrada adicionais na DLL do provedor de serviço sua mensagem. Para obter mais informações, consulte [Configurando um serviço de mensagem](configuring-a-message-service.md). Interface de configuração do provedor de repositório a mensagem é a única interface de usuário que um provedor de armazenamento de mensagem deve implementar.
  
## <a name="see-also"></a>Confira também



[Recursos de armazenamento de mensagens](message-store-features.md)

