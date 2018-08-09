---
title: Enviar ou receber uma mensagem sob demanda
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ece5340497f83862b711f076c8c6346e14ec9355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770367"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Enviar ou receber uma mensagem sob demanda
  
**Aplica-se a**: Outlook 
  
Os clientes normalmente dependem do subsistema de MAPI — o spooler MAPI e os provedores de serviço — para lidar com o tempo de transmissão de mensagem e recepção. No entanto, você pode alterar esse intervalo usando o objeto de status do spooler MAPI ou um provedor de transporte.
  
O método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) remove todas as mensagens das filas de entrada ou saída de um ou mais provedor de transporte. Os procedimentos a seguir descrevem duas técnicas para enviar ou receber mensagens sob demanda. O primeiro procedimento usa o objeto de status do spooler MAPI para liberar as filas de cada provedor de transporte no perfil; o segundo procedimento libera a fila de um provedor de transporte único. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Para liberar todas as filas de entrada ou saídas em uma única operação
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Chame o status método da tabela [IMAPITable::SetColumns](imapitable-setcolumns.md) para limitar a coluna definida como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Construa uma restrição de propriedade usando uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_RESOURCE_TYPE** com MAPI_SPOOLER. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura de **SPropertyRestriction** , para recuperar a linha que representa o status do spooler MAPI. 
    
5. Passe a coluna **PR_ENTRYID** para [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir objeto de status do spooler MAPI. 
    
6. Chame o método de [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) do spooler MAPI, passando o sinalizador FLUSH_NO_UI para suprimir a interface do usuário e o sinalizador o FLUSH_DOWNLOAD ou FLUSH_UPLOAD para liberar as filas de entrada ou de saída. 
    
7. Libere o objeto de status e a tabela de status, bem como a estrutura de [SRowSet](srowset.md) que é alocada para a tabela. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Para liberar as filas de entrada ou saídas individualmente pelo provedor de transporte
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Chame o status método da tabela [IMAPITable::SetColumns](imapitable-setcolumns.md) para limitar a coluna definida como **PR_ENTRYID** e **PR_RESOURCE_TYPE**.
    
3. Construa uma restrição de propriedade usando uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_RESOURCE_TYPE** com MAPI_TRANSPORT_PROVIDER. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura de **SPropertyRestriction** , para recuperar as linhas que forem fornecidas por provedores de transporte. 
    
5. Para cada linha retornada de **HrQueryAllRows**:
    
    1. Passe a coluna **PR_ENTRYID** para [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir o objeto de status do provedor de transporte. 
        
    2. Verifique se o objeto de status de transporte oferece suporte ao método **FlushQueues** , verificando se a sua propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tem o STATUS_FLUSH_QUEUES sinalizador será definido. 
        
    3. Se houver suporte, chame [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md). Se não suportado, chame o método de **IMAPIStatus::FlushQueues** do spooler MAPI, passando o identificador de entrada de transporte no parâmetro _lpTargetTransport_ . Consulte o procedimento anterior para obter instruções sobre como acessar o objeto de status do spooler MAPI. Defina o sinalizador FLUSH_DOWNLOAD para liberar as filas de saída ou o sinalizador FLUSH_UPLOAD para liberar as filas de entrada. 
        
    4. Libere o objeto de status e a tabela de status, bem como a estrutura de [SRowSet](srowset.md) que é alocada para a tabela. 
    
O MAPI spooler respeita o sinalizador FLUSH_NO_UI como a maioria dos provedores de transporte de LAN. No entanto, nem todos os provedores de transporte respeitam esse sinalizador, especialmente aqueles que usam um modem explicitamente e o serviço de acesso remoto (RAS). RAS não foi projetado para permitir que clientes suprimir a interface do usuário. É possível para um cliente ser configurado de forma que ele possa se conectar sem exigir a interação do usuário, mas é difícil e exige conhecimento profundo dos serviços de mensagem do cliente.
  

