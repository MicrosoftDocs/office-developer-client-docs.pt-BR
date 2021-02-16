---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432531"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Dá ao spooler MAPI acesso a um provedor de transporte. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Exposto por:  <br/> |Objetos de logon de transporte  <br/> |
|Implementado por:  <br/> |Provedores de transporte  <br/> |
|Chamado por:  <br/> |O spooler MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IXPLogon  <br/> |
|Tipo de ponteiro:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Retorna os tipos de destinatários que o provedor de transporte trata.  <br/> |
|**RegisterOptions** <br/> | *Sem suporte ou documentado.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Sinaliza a ocorrência de um evento sobre o qual o provedor de transporte solicitou a notificação.  <br/> |
|[Ocioso](ixplogon-idle.md) <br/> |Indica que o sistema está ocioso, permitindo que o provedor de transporte execute operações de baixa prioridade.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Inicia o processo de logoff.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indica que o spooler MAPI tem uma mensagem para o provedor de transporte entregar.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informa ao provedor de transporte que o spooler MAPI concluiu o processamento em uma mensagem de saída.  <br/> |
|[Sondagem](ixplogon-poll.md) <br/> |Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Abre o objeto de status do provedor de transporte.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Verifica o status externo do provedor de transporte.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Solicita que o provedor de transporte entregue imediatamente todas as mensagens de entrada ou de saída pendentes.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

