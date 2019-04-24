---
title: Recursos opcionais do provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: df38350b049264e7e20ac0bb821c71d93b992d2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348514"
---
# <a name="optional-transport-provider-features"></a>Recursos opcionais do provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de transporte de recursos opcionais podem ser implementados:
  
- Registro de opções de mensagens e destinatários específicas para o provedor de transporte.
    
- Manter um perfil, se necessário, para armazenar informações de configuração e credenciais no sistema de mensagens.
    
- Executar qualquer verificação de credenciais necessárias para o sistema de mensagens.
    
- Suporte à notificação de eventos para aplicativos clientes interessados com o método [IMAPISupport:: Notify](imapisupport-notify.md) . 
    
- Exibir folhas de propriedades de configuração e caixas de diálogo do assistente para permitir que os usuários definam as configurações do provedor de transporte.
    
- Fornecimento de relatórios de entrega de mensagens para aplicativos cliente.
    

