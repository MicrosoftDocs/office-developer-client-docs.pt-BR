---
title: Modelo de recebimento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 487598374f15300cc8b899a50d74b535b5a33c91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356942"
---
# <a name="message-reception-model"></a>Modelo de recebimento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O provedor de transporte controla se o spooler MAPI deve sondar o email de entrada ou se ele realiza uma chamada de volta ao spooler MAPI quando novos emails chegam. O provedor de transporte define o sinalizador SP_LOGON_POLL quando retorna de [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para solicitar a sondagem. Caso contrário, o provedor de transporte usará [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) quando o email de entrada estiver disponível. Após aprender que os emails de entrada estão disponíveis, o spooler MAPI abre uma nova mensagem e solicita que o provedor de transporte armazene as propriedades de mensagem recebidas na mensagem. 
  
Esse processo funciona da seguinte maneira:
  
1. As mensagens disponíveis são indicadas pelo provedor de transporte chamando **IMAPISupport:: SpoolerNotify** ou pelo spooler MAPI chamando [IXPLogon::P oll](ixplogon-poll.md).
    
2. O spooler MAPI chama [IXPLogon:: StartMessage](ixplogon-startmessage.md) para iniciar o processo. 
    
3. O provedor de transporte coloca um valor de referência no local referenciado no **StartMessage**. Esses valores de referência permitem que o provedor de transporte e o spooler MAPI acompanhem qual mensagem está sendo processada quando há várias mensagens a serem entregues.
    
4. O provedor de transporte armazena os dados da mensagem na instância aprovada [IMessage: IMAPIProp](imessageimapiprop.md) . 
    
5. O provedor de transporte chama o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) na instância **IMessage** e retorna de **StartMessage**.
    
6. O spooler MAPI chama [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) se ele deve parar a entrega de mensagens. 
    
> [!NOTE]
> Se um provedor de transporte deve fornecer um grande número de mensagens e o provedor de transporte estiver usando **IMAPISupport:: SpoolerNotify** em vez de **IXPLogon::P oll**, deve-se tomar cuidado para não chamar **SpoolerNotify** com muito frequência para não deprive outros provedores de transporte de tempo de CPU. O spooler MAPI tem lógica para evitar que isso aconteça, mas, em geral, o intervalo entre as chamadas **SpoolerNotify** deve ser maior do que o tempo que leva o seu provedor de transporte para processar uma mensagem. > também, o spooler MAPI pode não processar uma mensagem de entrada imediatamente. O MAPI spooler pode solicitar que o provedor de transporte execute outras tarefas antes de receber a mensagem de entrada. 
  

