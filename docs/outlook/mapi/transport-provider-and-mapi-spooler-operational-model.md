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
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594030"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Provedor de transporte e modelo operacional do spooler MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicialização do provedor de transporte, inicialização, processamento, desligamento e deinitialization são realizadas por uma série de chamadas do spooler MAPI para o provedor de transporte. As chamadas são sequenciadas da seguinte maneira:
  
1. O MAPI spooler chama a função [XPProviderInit](xpproviderinit.md) , passa um objeto de suporte, obtém o objeto de provedor e verifica se o provedor de transporte e o spooler MAPI suportam um números de versão do intervalo compatível de MAPI. 
    
2. O MAPI spooler chama o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) do [IXPProvider: IUnknown](ixpprovideriunknown.md) interface. Uma sessão é estabelecida entre o spooler MAPI e o provedor de transporte com as credenciais da seção atual do perfil. Provedor de transporte que retorna um objeto de logon. 
    
3. O MAPI spooler chama o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) . O provedor de transporte retorna uma lista de identificadores exclusivos (UIDs) e tipos de endereço de email serão aceitas. 
    
4. O provedor de transporte chama o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para criar sua linha na tabela de status de MAPI. 
    
5. O MAPI spooler chama o método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para habilitar o recebimento e transmissão de mensagens. 
    
6. Se solicitado pelo provedor de transporte em seu retorno para a chamada **TransportLogon** , o MAPI spooler periodicamente chama o método [IXPLogon::Idle](ixplogon-idle.md) . Processamento ocioso é útil se o provedor de transporte precisa sondar o sistema de mensagens subjacente para novas mensagens ou realize outras tarefas de baixa prioridade. 
    
7. O spooler MAPI e o provedor de transporte enviar e recebem mensagens. Para obter mais informações, consulte [Modelos de envio de mensagem](message-submission-model.md) e [recepção de mensagem](message-reception-model.md). O MAPI spooler chama em objetos de suporte, a mensagem e o anexo e solicitações de transporte de serviços.
    
8. O MAPI spooler chama o método de **TransportNotify** para desabilitar o recebimento e transmissão de mensagens. 
    
9. O MAPI spooler libera os objetos de logon e o provedor. Para obter mais informações, consulte o método [IXPProvider::Shutdown](ixpprovider-shutdown.md) . 
    

