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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404299"
---
# <a name="optional-transport-provider-features"></a>Recursos opcionais do provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de transporte de recursos opcionais podem implementar:
  
- Registrar opções de mensagem e destinatário específicas para o provedor de transporte.
    
- Manter um perfil, se necessário, para armazenar informações de configuração e credenciais no sistema de mensagens.
    
- Executar qualquer verificação das credenciais exigidas pelo sistema de mensagens.
    
- Suporte à notificação de evento para aplicativos cliente interessados com o [método IMAPISupport::Notify.](imapisupport-notify.md) 
    
- Exibir folhas de propriedades de configuração e caixas de diálogo do assistente para permitir que os usuários configurem as configurações do provedor de transporte.
    
- Fornecimento de relatórios de entrega de mensagens para aplicativos cliente.
    

