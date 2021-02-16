---
title: Modelo de Recepção de Mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415114"
---
# <a name="message-reception-model"></a>Modelo de Recepção de Mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O provedor de transporte controla se o spooler MAPI deve sondar o email de entrada ou se ele executa uma chamada de volta para o spooler MAPI quando novos emails chegam. O provedor de transporte define o SP_LOGON_POLL quando ele retorna de [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar sondagem. Caso contrário, o provedor de transporte [usará IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) quando o email de entrada estiver disponível. Depois de saber que o email de entrada está disponível, o spooler MAPI abre uma nova mensagem e pede ao provedor de transporte para armazenar as propriedades da mensagem recebida na mensagem. 
  
Esse processo funciona da seguinte forma:
  
1. As mensagens disponíveis são indicadas pelo provedor de transporte que chama **IMAPISupport::SpoolerNotify** ou pelo spooler MAPI chamando [IXPLogon::P oll.](ixplogon-poll.md)
    
2. O spooler MAPI chama [IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar o processo. 
    
3. O provedor de transporte coloca um valor de referência no local referenciado em **StartMessage**. Esses valores de referência permitem que o provedor de transporte e o spooler MAPI acompanhem qual mensagem está sendo processada quando há várias mensagens a serem entregues.
    
4. O provedor de transporte armazena os dados da mensagem na [instância IMessage : IMAPIProp](imessageimapiprop.md) passada. 
    
5. O provedor de transporte chama o [método IMAPIProp::SaveChanges](imapiprop-savechanges.md) na instância **IMessage** e retorna de **StartMessage**.
    
6. O spooler MAPI chama [IXPLogon::TransportNotify](ixplogon-transportnotify.md) se for necessário interromper a entrega da mensagem. 
    
> [!NOTE]
> Se um provedor de transporte deve entregar um grande número de mensagens e o provedor de transporte estiver usando **IMAPISupport::SpoolerNotify** em vez de **IXPLogon::P oll**, deve ser cuidado para não chamar **SpoolerNotify** com muita frequência para não se preocupar com outros provedores de transporte de tempo de CPU. O spooler MAPI tem lógica para evitar que isso aconteça, mas, em geral, o intervalo entre as chamadas **SpoolerNotify** deve ser maior do que o tempo necessário para o provedor de transporte processar uma mensagem. >, o spooler MAPI pode não processar uma mensagem de entrada imediatamente. O spooler MAPI pode pedir ao provedor de transporte para executar outras tarefas antes de receber a mensagem de entrada. 
  

