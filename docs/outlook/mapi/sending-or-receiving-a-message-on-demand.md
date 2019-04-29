---
title: Enviar ou receber uma mensagem sob demanda
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436367"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>Enviar ou receber uma mensagem sob demanda
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Geralmente, os clientes dependem do subsistema MAPI, o spooler MAPI e os provedores de serviços para lidar com a temporização de transmissão de mensagens e recebimento. No enTanto, você pode alterar esse intervalo usando o objeto status do spooler MAPI ou de um provedor de transporte.
  
O método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) remove todas as mensagens de uma ou mais filas de entrada ou saída do provedor de transporte. Os procedimentos a seguir descrevem duas técnicas de envio ou recebimento de mensagens sob demanda. O primeiro procedimento usa o objeto status do spooler MAPI para liberar as filas de cada provedor de transporte no perfil; o segundo procedimento libera a fila de um único provedor de transporte. 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>Para liberar todas as filas de entrada ou saída em uma única operação
  
1. Chame [IMAPISession::](imapisession-getstatustable.md) getstatustable para acessar a tabela status. 
    
2. Chame o método imApitable da tabela de status [::](imapitable-setcolumns.md) SetColumns para limitar o conjunto de colunas a **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).
    
3. Criar uma restrição de propriedade usando uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder ao **PR_RESOURCE_TYPE** com o MAPI_SPOOLER. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura **SPropertyRestriction** , para recuperar a linha que representa o status do spooler MAPI. 
    
5. Passe a coluna **PR_ENTRYID** para [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir o objeto status do spooler do MAPI. 
    
6. Chame o método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) do spooler MAPI, passando o sinalizador FLUSH_NO_UI para suprimir a interface do usuário e o sinalizador FLUSH_DOWNLOAD ou FLUSH_UPLOAD para liberar as filas de saída ou de entrada. 
    
7. Liberar o objeto status e a tabela status, bem como a estrutura [SRowSet](srowset.md) alocada para a tabela. 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>Para liberar filas de entrada ou de saída individualmente por provedor de transporte
  
1. Chame [IMAPISession::](imapisession-getstatustable.md) getstatustable para acessar a tabela status. 
    
2. Chame o método imApitable da tabela de status [::](imapitable-setcolumns.md) SetColumns para limitar o conjunto de colunas ao **PR_ENTRYID** e ao **PR_RESOURCE_TYPE**.
    
3. Criar uma restrição de propriedade usando uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder ao **PR_RESOURCE_TYPE** com o MAPI_TRANSPORT_PROVIDER. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura **SPropertyRestriction** , para recuperar as linhas que são fornecidas pelos provedores de transporte. 
    
5. Para cada linha retornada de **HrQueryAllRows**:
    
    1. Passe a coluna **PR_ENTRYID** para [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir o objeto status do provedor de transporte. 
        
    2. Verifique se o objeto de status de transporte oferece suporte ao método **FlushQueues** verificando se sua propriedade **PR_RESOURCE_METHODS** ([PIDTAGRESOURCEMETHODS](pidtagresourcemethods-canonical-property.md)) tem o sinalizador STATUS_FLUSH_QUEUES definido. 
        
    3. Se houver suporte, chame [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md). Se não houver suporte, chame o método **IMAPIStatus:: FlushQueues** do spooler MAPI, passando o identificador de entrada do transporte no parâmetro _lpTargetTransport_ . Consulte o procedimento anterior para obter instruções sobre como acessar o objeto status do spooler MAPI. Defina o sinalizador FLUSH_DOWNLOAD para liberar as filas de saída ou o sinalizador FLUSH_UPLOAD para liberar as filas de entrada. 
        
    4. Liberar o objeto status e a tabela status, bem como a estrutura [SRowSet](srowset.md) alocada para a tabela. 
    
O spooler MAPI honra o sinalizador FLUSH_NO_UI como a maioria dos provedores de transporte de LAN. No enTanto, nem todos os provedores de transporte honram esse sinalizador, particularmente aqueles que usam um modem explicitamente e o serviço de acesso remoto (RAS). O RAS não foi projetado para permitir que os clientes suprimem a interface do usuário. É possível que um cliente seja configurado para que ele possa se conectar sem exigir a interação de um usuário, mas é difícil e exige conhecimento profundo dos serviços de mensagens do cliente.
  

