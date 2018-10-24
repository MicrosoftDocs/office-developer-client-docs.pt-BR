---
title: Desligar um provedor do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e38219db-f867-4c1d-9973-0e025779e8b6
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8e4712572eaff465bb23b55eccc3670f637c0f9c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386048"
---
# <a name="shutting-down-a-message-store-provider"></a>Desligar um provedor do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se seu provedor for um provedor de armazenamento de mensagem, ele pode ser desligado em uma das seguintes maneiras:
  
- Quando um cliente ou o MAPI spooler chama [IMsgStore::StoreLogoff](imsgstore-storelogoff.md). Encerrando um provedor de armazenamento de mensagem com **StoreLogoff** faz com que o desligamento ocorra uma maneira ordenada e controlada. 
    
- Quando um cliente chama [IMAPISession::Logoff](imapisession-logoff.md). 
    
A implementação dos **IMsgStore::StoreLogoff** deve começar chamando [IMAPISupport::StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar MAPI que está sendo desligado, indicando que qualquer provedor de transporte relacionados deve ser desconectado. Quando **IMsgStore::StoreLogoff** retorna, seu chamador chama o método de [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do seu armazenamento de mensagens. Implemente esse método **versão** chamando-se o suporte ao método do objeto **IUnknown:: Release** . 
  
MAPI executa as seguintes tarefas em sua implementação do **IUnknown:: Release** para repositórios de mensagem: 
  
1. Remove todas as estruturas [MAPIUID](mapiuid.md) registradas pelo provedor de armazenamento de mensagem. 
    
2. Remove a linha do provedor de repositório a mensagem da tabela de status.
    
3. Chama [IMSLogon::Logoff](imslogon-logoff.md) para liberar todos os objetos abertos, subobjetos e objetos de status. 
    
4. Chama [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto de logon do provedor de repositório a mensagem. 
    
Alguns clientes podem omitir a chamada para **IMsgStore::StoreLogoff**, iniciando o desligamento do seu provedor de armazenamento de mensagem com a chamada ao método de **IUnknown:: Release** do armazenamento de mensagens. Um desligamento seguintes circunstâncias sem a chamada para **StoreLogoff** é menos ordenado e controlada. Escreva o método de **lançamento** do armazenamento de suas mensagens para lidar com essa possibilidade e ficar atento se ou não uma chamada para **IMAPISupport::StoreLogoffTransports** ocorreu. **StoreLogoffTransports** deve ser chamada uma vez durante o processo de desligamento. Se você detectar no seu método de **versão** que **StoreLogoffTransports** ainda não foi chamado, chamá-la com o sinalizador LOGOFF_ABORT. 
  
## <a name="see-also"></a>Confira também



[Encerrando um provedor de serviços](shutting-down-a-service-provider.md)

