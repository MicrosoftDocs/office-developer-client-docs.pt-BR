---
title: Visão geral da arquitetura do MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a0f2efc17ca8790502f11d677498013cbe10205d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579351"
---
# <a name="mapi-architecture-overview"></a>Visão geral da arquitetura do MAPI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define uma arquitetura modular, conforme mostrado na ilustração a seguir.  
  
![Arquitetura do Outlook 2010] (media/amapi_43.gif "Arquitetura do Outlook 2010")
  
O aplicativo de MAPI é conhecido como um aplicativo cliente porque ele é um cliente do subsistema de MAPI. Aplicativos baseados em mensagens empregam como parte central do seu processamento de mensagens e oferecem recursos de mensagens extensivo, como a troca de informações de diversos tipos em vários formatos e a capacidade de salvar e organizar as informações localmente. Envie um email, agendar, e aplicativos de fluxo de trabalho são exemplos de aplicativos baseados em mensagens.
  
O subsistema de MAPI é composto por uma interface de usuário comum e as interfaces de programação. A interface de usuário comum é um conjunto de caixas de diálogo que proporciona aos aplicativos cliente uma aparência consistente e usuários uma maneira consistente de trabalhar.
  
MAPI tem interfaces de programação que são usados pelo subsistema de MAPI, por desenvolvedores de software do cliente e por desenvolvedores de provedor de serviço. A interface de programação de MAPI é a interface de programação baseada no objeto principal. A interface de programação de MAPI é semelhante ao OLE Component Object Model e é usada pelo subsistema MAPI e aplicativos de cliente baseado em mensagens escritos em C ou C++. 
  
Como um desenvolvedor de software do cliente, você pode fazer chamadas MAPI diretamente por meio da interface de programação de MAPI. Você pode implementar a mensagens com uma única interface de cliente MAPI ou uma combinação das interfaces. Um único aplicativo pode fazer chamadas para métodos ou funções que pertencem a qualquer uma das interfaces.
  
## <a name="see-also"></a>Confira também

-[Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

