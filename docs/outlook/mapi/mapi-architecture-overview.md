---
title: Visão geral da arquitetura MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 00d2993c-d66a-4a00-9fb2-98696d29a007
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 98a723528a714918ad7e0f10534efb0d38ef139a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410074"
---
# <a name="mapi-architecture-overview"></a>Visão geral da arquitetura MAPI
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI define uma arquitetura modular, conforme mostrado na ilustração a seguir.  
  
![Arquitetura do Outlook 2010 Arquitetura](media/amapi_43.gif "do Outlook 2010")
  
O aplicativo MAPI é conhecido como um aplicativo cliente porque é um cliente do subsistema MAPI. Aplicativos baseados em mensagens empregam mensagens como parte central de seu processamento e oferecem recursos extensivos de mensagens, como a troca de informações de vários tipos em vários formatos e a capacidade de salvar e organizar as informações localmente. Aplicativos de email, agendamento e fluxo de trabalho são exemplos de aplicativos baseados em mensagens.
  
O subsistema MAPI é feito de uma interface de usuário comum e das interfaces de programação. A interface do usuário comum é um conjunto de caixas de diálogo que dá aos aplicativos cliente uma aparência consistente e aos usuários uma maneira consistente de trabalhar.
  
MAPI has programming interfaces that are used by the MAPI subsystem, by client software developers, and by service provider developers. A interface de programação MAPI é a principal interface de programação baseada em objeto. A interface de programação MAPI é semelhante ao Modelo de Objeto de Componente OLE e é usada pelo subsistema MAPI e aplicativos cliente baseados em mensagens escritos em C ou C++. 
  
Como desenvolvedor de software cliente, você faz chamadas MAPI diretamente por meio da interface de programação MAPI. Você pode implementar mensagens com uma única interface de cliente MAPI ou uma combinação de interfaces. Um único aplicativo pode fazer chamadas a métodos ou funções pertencentes a qualquer uma das interfaces.
  
## <a name="see-also"></a>Confira também

-[Arquitetura e recursos de MAPI](mapi-features-and-architecture.md)

