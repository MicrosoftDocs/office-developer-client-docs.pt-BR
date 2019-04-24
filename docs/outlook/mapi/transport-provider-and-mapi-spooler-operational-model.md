---
title: Provedor de transporte e modelo operacional do spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356606"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Provedor de transporte e modelo operacional do spooler MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A inicialização, inicialização, processamento, desligamento e desinicialização do provedor de transporte são realizadas por uma série de chamadas do spooler MAPI para o provedor de transporte. As chamadas são sequenciadas da seguinte maneira:
  
1. O spooler MAPI chama a função [XPProviderInit](xpproviderinit.md) , passa um objeto support, obtém o objeto Provider e verifica se o provedor de transporte e o spooler MAPI dão suporte a um intervalo compatível de números de versão MAPI. 
    
2. O spooler MAPI chama o método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) da interface [IXPProvider: IUnknown](ixpprovideriunknown.md) . Uma sessão é estabelecida entre o spooler MAPI e o provedor de transporte com as credenciais da seção atual do perfil. O provedor de transporte retorna um objeto de logon. 
    
3. O spooler MAPI chama o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . O provedor de transporte retorna uma lista de identificadores exclusivos (UIDs) e tipos de endereço de email que ele aceitará. 
    
4. O provedor de transporte chama o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para criar sua linha na tabela de status MAPI. 
    
5. O spooler MAPI chama o método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) para habilitar a transmissão de mensagens e a recepção. 
    
6. Se solicitado pelo provedor de transporte em seu retorno para a chamada **TransportLogon** , o spooler MAPI chama periodicamente o método [IXPLogon:: Idle](ixplogon-idle.md) . O processamento de ociosidade é útil quando o provedor de transporte precisa sondar o sistema de mensagens subjacente para novas mensagens ou executar outras tarefas de baixa prioridade. 
    
7. O spooler MAPI e o provedor de transporte enviam e recebem mensagens. Para obter mais informações, consulte o [modelo de envio de mensagens](message-submission-model.md) e o modelo de recebimento de [mensagens](message-reception-model.md). Os serviços de spooler MAPI reportam solicitações e chamadas em objetos de suporte, mensagem e anexo.
    
8. O spooler MAPI chama o método **TransportNotify** para desabilitar a transmissão de mensagens e a recepção. 
    
9. O spooler MAPI libera os objetos de logon e provedor. Para obter mais informações, consulte o método [IXPProvider:: Shutdown](ixpprovider-shutdown.md) . 
    

