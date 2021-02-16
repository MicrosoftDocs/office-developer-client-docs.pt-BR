---
title: Visão geral do provedor de serviços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: bc25158daa9579b5cd6cebe1eee878bf087762a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431425"
---
# <a name="mapi-service-provider-overview"></a>Visão geral do provedor de serviços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Entre o subsistema MAPI e os sistemas de mensagens estão os vários provedores de serviços. Os provedores de serviços são como drivers que conectam aplicativos cliente MAPI a um sistema de mensagens subjacente. Há três tipos de provedores: provedores de armazenamento de mensagens, de agenda ou de diretório e de transporte de mensagens. O MAPI dá suporte a cada tipo de serviço independentemente, permitindo que um fornecedor ofereça um ou mais provedores de serviços personalizados. Por exemplo, um fornecedor pode querer criar um provedor de agendamento de endereços que use um diretório de agendamento telefônico corporativo de funcionários ou para criar um provedor de armazenamento de mensagens que use um banco de dados existente.
  
Os provedores de serviços geralmente são escritos para sistemas de mensagens específicos por desenvolvedores de software que têm conhecimento especializado ou experiência com um sistema específico. For example, the Microsoft Outlook 2013 and Microsoft Outlook 2010 Mobile Services use an address book provider to expose a mobile address book in Outlook. 
  
MAPI presents client applications with a unified view of address book and transport provider information. Essa abordagem integrada impede que o aplicativo cliente tenha que mapear dados para o provedor apropriado. Ele também impede que o usuário tenha que negociar entre vários esquemas de endereçamento do address book e do provedor de transporte. No entanto, as informações do provedor do armazenamento de mensagens não são unificadas, e os clientes que usam vários provedores de armazenamento de mensagens são responsáveis por lidar com eles individualmente.
  
Os provedores de serviços trabalham com MAPI para criar e enviar mensagens da seguinte maneira: as mensagens são criadas usando um formulário apropriado para o tipo específico, ou classe, da mensagem. Muitas mensagens são feitas com o formulário de anotação padrão que vem com o subsistema MAPI, seja pelo usuário de um aplicativo cliente ou programaticamente sem a interação do usuário. A mensagem concluída é endereçada a um ou mais destinatários um usuário ou grupo de usuários designados para receber a mensagem. Um destinatário pode ou não ter uma entrada em um diretório que pertence a um dos provedores de agendas instalados. Destinatários que não estão associados a um provedor de agendas de endereços instalado são chamados de destinatários personalizados ou endereços exclusivos. Um endereço único pode ser temporário, durando apenas até que a mensagem seja enviada. 
  
Quando o aplicativo cliente envia a mensagem, o provedor do armazenamento de mensagens verifica se cada destinatário tem um endereço exclusivo e válido e se a mensagem tem todas as informações necessárias para transmissão. Se houver uma pergunta sobre um destinatário (por exemplo, quando houver vários destinatários com o mesmo nome), um provedor de agendamento se preocupará em resolver a ambiguidade. Em seguida, a mensagem é colocada na fila de saída. 
  
## <a name="see-also"></a>Confira também



[Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

