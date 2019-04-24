---
title: DesLigando um provedor de repositório de mensagens
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
# <a name="shutting-down-a-message-store-provider"></a>DesLigando um provedor de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se seu provedor é um provedor de repositório de mensagens, ele pode ser desligado de uma das seguintes maneiras:
  
- Quando um cliente ou o spooler MAPI chama [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md). O desligamento de um provedor de repositório de mensagens com o **StoreLogoff** faz com que o desligamento ocorra de forma ordenada e controlada. 
    
- Quando um cliente chama [IMAPISession:: logoff](imapisession-logoff.md). 
    
Sua implementação do **IMsgStore:: StoreLogoff** deve começar chamando [IMAPISupport:: StoreLogoffTransports](imapisupport-storelogofftransports.md) para informar ao MAPI que ele está sendo desligado, indicando que qualquer provedor de transporte relacionado deve ser desconectado. Quando **IMsgStore:: StoreLogoff** retorna, seu chamador invoca o método [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do repositório de mensagens. Implemente este método de **versão** chamando o método **IUnknown:: Release** do objeto support. 
  
O MAPI realiza as seguintes tarefas em sua implementação de **IUnknown:: Release** for Message Stores: 
  
1. Remove todas as estruturas [MAPIUID](mapiuid.md) registradas pelo provedor de armazenamento de mensagens. 
    
2. Remove a linha do provedor de repositório de mensagens da tabela de status.
    
3. Chama [IMSLogon:: logoff](imslogon-logoff.md) para liberar todos os objetos, subobjetos e objetos de status abertos. 
    
4. Chama [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para liberar o objeto de logon do provedor de repositório de mensagens. 
    
Alguns clientes podem omitir a chamada para **IMsgStore:: StoreLogoff**, iniciando o desligamento do seu provedor de repositório de mensagens com a chamada para o método **IUnknown:: Release** do repositório de mensagens. Um desligamento sob essas circunstâncias sem a chamada para **StoreLogoff** é menos ordenada e controlado. Escreva o método de **lançamento** do seu repositório de mensagens para lidar com essa possibilidade e acompanhar se uma chamada para **IMAPISupport:: StoreLogoffTransports** ocorreu ou não. **StoreLogoffTransports** deve ser chamado uma vez durante o processo de desligamento. Se você detectar no seu método de **versão** que o **StoreLogoffTransports** ainda não foi chamado, invoque-o com o sinalizador LOGOFF_ABORT. 
  
## <a name="see-also"></a>Confira também



[Desligar um provedor de serviços](shutting-down-a-service-provider.md)

