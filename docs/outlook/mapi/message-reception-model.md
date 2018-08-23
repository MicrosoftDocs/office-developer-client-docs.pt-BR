---
title: Modelo de recebimento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8fbc09d9d79f88ef783b8effe7a24e4b35564cee
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570370"
---
# <a name="message-reception-model"></a>Modelo de recebimento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O provedor de transporte controla se o MAPI spooler deve sondá-lo para email de entrada ou se ele realiza uma chamada de volta para o MAPI spooler quando chegar novo email. O provedor de transporte define o sinalizador SP_LOGON_POLL quando ela retorna de [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar sondagem. Caso contrário, o provedor de transporte usa [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) quando o email de entrada estiver disponível. Depois que o email de entrada está disponível de aprendizagem, o MAPI spooler abre uma nova mensagem e solicita o provedor de transporte para armazenar as propriedades da mensagem recebida na mensagem. 
  
Esse processo funciona da seguinte maneira:
  
1. Mensagens disponíveis são indicadas pelo provedor de transporte chamar **IMAPISupport::SpoolerNotify** ou pelo spooler MAPI chamar [IXPLogon::Poll](ixplogon-poll.md).
    
2. O MAPI spooler chama [IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar o processo. 
    
3. O provedor de transporte coloca um valor de referência no local referenciado na **StartMessage**. Esses valores de referência permitem que o provedor de transporte e o spooler MAPI controlar qual mensagem está sendo processada quando há várias mensagens para fornecer.
    
4. Provedor de transporte que armazena os dados de mensagem no passado. [IMessage: IMAPIProp](imessageimapiprop.md) instância. 
    
5. O provedor de transporte chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na instância **IMessage** e retorna a partir de **StartMessage**.
    
6. O MAPI spooler chama [IXPLogon::TransportNotify](ixplogon-transportnotify.md) se ele deve parar a entrega da mensagem. 
    
> [!NOTE]
> Se um provedor de transporte deve fornecer um grande número de mensagens e o provedor de transporte está usando **IMAPISupport::SpoolerNotify** em vez de **IXPLogon::Poll**, tome cuidado não para chamar **SpoolerNotify** muito frequentemente na ordem não fazer impedir que outros provedores de transporte do tempo da CPU. O MAPI spooler possuem lógica para evitar que isso aconteça, mas, em geral, o intervalo entre chamadas **SpoolerNotify** deve ser maior que o tempo que leva seu provedor de transporte para processar uma mensagem. > Além disso, o MAPI spooler talvez não processar uma mensagem de entrada imediatamente. O MAPI spooler pode solicitar que o provedor de transporte para executar outras tarefas antes de ele recebe a mensagem de entrada. 
  

