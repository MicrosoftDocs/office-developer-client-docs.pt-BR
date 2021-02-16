---
title: Provedor de Transporte e Modelo Operacional do Spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426622"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Provedor de Transporte e Modelo Operacional do Spooler MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A inicialização, a inicialização, o processamento, o desligamento e a inicialização do provedor de transporte são realizadas por uma série de chamadas do spooler MAPI para o provedor de transporte. As chamadas são sequenciadas da seguinte forma:
  
1. O spooler MAPI chama a função [XPProviderInit,](xpproviderinit.md) passa um objeto de suporte, obtém o objeto do provedor e verifica se o provedor de transporte e o spooler MAPI suportam um intervalo compatível de números de versão MAPI. 
    
2. O spooler MAPI chama o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) da interface [IXPProvider : IUnknown.](ixpprovideriunknown.md) Uma sessão é estabelecida entre o spooler MAPI e o provedor de transporte com as credenciais na seção atual do perfil. O provedor de transporte retorna um objeto de logon. 
    
3. O spooler MAPI chama o [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md) O provedor de transporte retorna uma lista dos identificadores exclusivos (UIDs) e tipos de endereço de email que ele aceitará. 
    
4. O provedor de transporte chama o [método IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para criar sua linha na tabela de status MAPI. 
    
5. O spooler MAPI chama o [método IXPLogon::TransportNotify](ixplogon-transportnotify.md) para habilitar a transmissão e a recepção de mensagens. 
    
6. Se solicitado pelo provedor de transporte em seu retorno para a chamada **TransportLogon,** o spooler MAPI chama periodicamente o método [IXPLogon::Idle.](ixplogon-idle.md) O processamento ocioso será útil se o provedor de transporte precisar sondar o sistema de mensagens subjacente em busca de novas mensagens ou realizar outras tarefas de baixa prioridade. 
    
7. O spooler MAPI e o provedor de transporte enviam e recebem mensagens. Para obter mais informações, consulte [Modelo de Envio de Mensagem](message-submission-model.md) e Modelo de Recepção de [Mensagens.](message-reception-model.md) O spooler mapi serviços de transporte solicitações e chamadas em objetos de suporte, mensagem e anexo.
    
8. O spooler MAPI chama o **método TransportNotify** para desabilitar a transmissão e a recepção de mensagens. 
    
9. O spooler MAPI libera os objetos de logon e provedor. Para obter mais informações, consulte o [método IXPProvider::Shutdown.](ixpprovider-shutdown.md) 
    

