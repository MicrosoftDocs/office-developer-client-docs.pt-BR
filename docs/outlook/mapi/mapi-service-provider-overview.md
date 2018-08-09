---
title: Visão geral do provedor de serviço MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7cbc79f-3d60-4f21-a378-7b0088ee8ad3
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 15a53a0bb16db3683e4c1320ac2e54648c8c697b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767950"
---
# <a name="mapi-service-provider-overview"></a>Visão geral do provedor de serviço MAPI

  
  
**Aplica-se a**: Outlook 
  
Entre os sistemas de mensagens e o subsistema de MAPI são os vários provedores de serviço. Provedores de serviços são como drivers que se conectam a aplicativos de cliente MAPI para um sistema de mensagens subjacente. Existem três tipos de provedores: provedores de armazenamento, catálogo de endereços ou provedores de diretório e provedores de transporte de mensagem de mensagem. MAPI oferece suporte a cada tipo de serviço de forma independente, permitindo que um fornecedor a oferecer um ou mais provedores de serviço personalizado. Por exemplo, um fornecedor pode querer para criar um provedor de catálogo de endereços que usa um diretório corporativo catálogo de telefone de funcionários ou para criar um provedor de armazenamento de mensagem que usa um banco de dados existente.
  
Provedores de serviço geralmente são gravadas para sistemas de mensagens específicos por desenvolvedores de software que tenham conhecimento especializado ou experiência com um sistema específico. Por exemplo, o Microsoft Outlook 2013 e os serviços do Microsoft Outlook 2010 Mobile usam um provedor de catálogo de endereços para expor um catálogo de endereços móvel no Outlook. 
  
MAPI apresenta os aplicativos de cliente com uma exibição unificada de informações do provedor de transporte e o catálogo de endereços. Essa abordagem integrada impede que o aplicativo cliente precisar mapear dados para o provedor apropriado. Ele também impede que o usuário precisar negociar entre vários catálogo de endereços e esquemas de endereçamento de provedor de transporte. Informações do provedor de repositório de mensagem, no entanto, não estão unificadas, e os clientes que usam vários provedores de armazenamento de mensagem são responsáveis por tratá-las individualmente.
  
Provedores de serviços de trabalham com MAPI para criar e enviar mensagens da seguinte maneira: mensagens são criadas usando-se um formulário que é apropriado para o tipo específico ou classe da mensagem. Muitas mensagens são feitas com o formulário Observação padrão que acompanha o subsistema de MAPI, pelo usuário de um aplicativo cliente ou programaticamente sem interação do usuário. A mensagem concluída endereçada a um ou mais destinatários — um usuário ou grupo de usuários designado para receber a mensagem. Um destinatário pode ou pode não ter uma entrada em um diretório que possui por um dos provedores de catálogo de endereços instalada. Destinatários que não estiverem associados um provedor de catálogo de endereços instalados são chamados destinatários personalizados ou endereços únicos. Um endereço único pode ser temporário que dura até que a mensagem é enviada. 
  
Quando o aplicativo cliente envia a mensagem, o provedor de armazenamento de mensagem verifica se cada destinatário tem um endereço válido e exclusivo e que a mensagem tem todas as informações necessárias para a transmissão. Se houver uma pergunta sobre um destinatário (por exemplo, quando há vários destinatários com o mesmo nome), um fornecedor de catálogo de endereços cuida de resolver a ambiguidade. Em seguida, a mensagem é colocada na fila de saída. 
  
## <a name="see-also"></a>Confira também



[Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

