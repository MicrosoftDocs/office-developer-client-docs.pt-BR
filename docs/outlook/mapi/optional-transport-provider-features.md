---
title: Recursos do provedor de transporte opcional
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: fd685e5bc67a3cb0785d9102e94c11ea921f07ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768185"
---
# <a name="optional-transport-provider-features"></a>Recursos do provedor de transporte opcional

  
  
**Aplica-se a**: Outlook 
  
Provedores de transporte podem implementar os recursos opcionais incluem:
  
- Registrando a mensagem e destinatários opções específicas para o provedor de transporte.
    
- Mantendo um perfil, se necessário, para armazenar informações de configuração e as credenciais para o sistema de mensagens.
    
- Executar qualquer verificação de credenciais exigidos pelo sistema de mensagens.
    
- Notificação de evento de suporte para aplicativos de cliente interessado com o método [IMAPISupport::Notify](imapisupport-notify.md) . 
    
- Exibindo as folhas de propriedades de configuração e caixas de diálogo Assistente para habilitar usuários definir configurações do provedor de transporte.
    
- Fornecimento de relatórios de entrega de mensagem para os aplicativos cliente.
    

