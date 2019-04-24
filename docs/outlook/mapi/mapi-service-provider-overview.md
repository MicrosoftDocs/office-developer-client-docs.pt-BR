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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339967"
---
# <a name="mapi-service-provider-overview"></a>Visão geral do provedor de serviços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Entre o subsistema MAPI e os sistemas de mensagens são vários provedores de serviços. Os provedores de serviços são como drivers que conectam aplicativos cliente MAPI a um sistema de mensagens subjacente. Há três tipos de provedores: provedores de repositórios de mensagens, catálogo de endereços ou provedores de diretório e provedores de transporte de mensagens. O MAPI oferece suporte a cada tipo de serviço de forma independente, permitindo que um fornecedor ofereça um ou mais provedores de serviços personalizados. Por exemplo, um fornecedor pode querer criar um provedor de catálogo de endereços que usa um diretório de catálogo telefônico corporativo de funcionários ou para criar um provedor de repositório de mensagens que usa um banco de dados existente.
  
Os provedores de serviços são normalmente escritos para sistemas de mensagens específicos por desenvolvedores de software com conhecimento especializado ou experiência com um sistema específico. Por exemplo, os serviços móveis do Microsoft Outlook 2013 e do Microsoft Outlook 2010 usam um provedor de catálogo de endereços para expor um catálogo de endereços móvel no Outlook. 
  
O MAPI apresenta aos aplicativos cliente uma visão unificada das informações do catálogo de endereços e do provedor de transporte. Essa abordagem integrada impede que o aplicativo cliente tenha que mapear dados para o provedor apropriado. Também impede que o usuário tenha que negociar entre vários esquemas de endereçamento de catálogo de endereços e de provedor de transporte. No entanto, as informações do provedor de repositório de mensagens não são unificadas, e os clientes que usam vários provedores de repositório de mensagens são responsáveis por tratá-los individualmente.
  
Os provedores de serviços trabalham com MAPI para criar e enviar mensagens da seguinte maneira: as mensagens são criadas usando um formulário apropriado para o tipo específico ou a classe de Message. Muitas mensagens são feitas com o formulário de anotação padrão que vem com o subsistema MAPI, seja pelo usuário de um aplicativo cliente ou via programação sem interação do usuário. A mensagem concluída é endereçada a um ou mais destinatários — um usuário ou grupo de usuários designados para receber a mensagem. Um destinatário pode ou não ter uma entrada em um diretório proprietário de um dos provedores de catálogo de endereços instalados. Os destinatários que não estão associados a um provedor de catálogo de endereços instalado são chamados de destinatários personalizados ou endereços de one-off. Um endereço one-off pode ser temporário, com o fim de mais duradouro até que a mensagem seja enviada. 
  
Quando o aplicativo cliente envia a mensagem, o provedor de armazenamento de mensagens verifica se cada destinatário tem um endereço exclusivo e válido e se a mensagem tem todas as informações necessárias para transmissão. Se houver uma dúvida sobre um destinatário (por exemplo, quando há vários destinatários com o mesmo nome), um provedor de catálogo de endereços cuida da resolução da ambigüidade. A mensagem é colocada na fila de saída. 
  
## <a name="see-also"></a>Confira também



[Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

