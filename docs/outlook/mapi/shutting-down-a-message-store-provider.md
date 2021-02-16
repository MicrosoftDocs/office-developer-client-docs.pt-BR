---
title: Desligar um provedor de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339197"
---
# <a name="shutting-down-a-message-store-provider"></a>Desligar um provedor de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se o provedor for um provedor de armazenamento de mensagens, ele poderá ser desligado de uma das seguintes maneiras:
  
- Quando um cliente ou o spooler MAPI chama [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). Desligar um provedor de armazenamento de mensagens **com StoreLogoff** faz com que o desligamento ocorra de maneira organizada e controlada. 
    
- Quando um cliente chama [IMAPISession::Logoff](imapisession-logoff.md). 
    
Sua implementação do **IMsgStore::StoreLogoff** deve começar chamando [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar ao MAPI que ele está sendo desligado, indicando que qualquer provedor de transporte relacionado deve ser desconectado. Quando **IMsgStore::StoreLogoff** retorna, o chamador invoca o método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do repositório de mensagens. Implemente **esse método Release** chamando o método **IUnknown::Release do** objeto de suporte. 
  
O MAPI executa as seguintes tarefas em sua implementação **de IUnknown::Release** para armazenamentos de mensagens: 
  
1. Remove todas as estruturas [MAPIUID](mapiuid.md) registradas pelo provedor de armazenamento de mensagens. 
    
2. Remove a linha do provedor de armazenamento de mensagens da tabela de status.
    
3. Chama [IMSLogon::Logoff](imslogon-logoff.md) para liberar todos os objetos abertos, subobjetos e objetos de status. 
    
4. Chama [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto de logon do provedor de armazenamento de mensagens. 
    
Alguns clientes podem omitir a chamada para **IMsgStore::StoreLogoff**, iniciando o desligamento do seu provedor de repositório de mensagens com a chamada para o método **IUnknown::Release** do repositório de mensagens. Um desligamento sob essas circunstâncias sem a chamada para **StoreLogoff** é menos pedido e controlado. Escreva o método  Release do seu armazenamento de mensagens para lidar com essa possibilidade e acompanhar se ocorreu ou não uma chamada para **IMAPISupport::StoreLogoffTransports.** **StoreLogoffTransports** deve ser chamado uma vez durante o processo de desligamento. Se você detectar no **método Release** que **StoreLogoffTransports** ainda não foi chamado, invoque-o com o sinalizador LOGOFF_ABORT usuário. 
  
## <a name="see-also"></a>Confira também



[Desligar um provedor de serviços](shutting-down-a-service-provider.md)

