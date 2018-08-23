---
title: Recursos opcionais do provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b55e6518ee1f3f59ef0459b3aeb68461f00a7ab3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566821"
---
# <a name="optional-transport-provider-features"></a>Recursos opcionais do provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de transporte podem implementar os recursos opcionais incluem:
  
- Registrando a mensagem e destinatários opções específicas para o provedor de transporte.
    
- Mantendo um perfil, se necessário, para armazenar informações de configuração e as credenciais para o sistema de mensagens.
    
- Executar qualquer verificação de credenciais exigidos pelo sistema de mensagens.
    
- Notificação de evento de suporte para aplicativos de cliente interessado com o método [IMAPISupport::Notify](imapisupport-notify.md) . 
    
- Exibindo as folhas de propriedades de configuração e caixas de diálogo Assistente para habilitar usuários definir configurações do provedor de transporte.
    
- Fornecimento de relatórios de entrega de mensagem para os aplicativos cliente.
    

