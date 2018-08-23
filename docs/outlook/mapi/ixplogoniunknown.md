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
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581402"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Concede o acesso de spooler MAPI para um provedor de transporte. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Expostos pelo:  <br/> |Objetos de logon de transporte  <br/> |
|Implementada por:  <br/> |Provedores de transporte  <br/> |
|Chamado pelo:  <br/> |O MAPI spooler  <br/> |
|Identificador de interface:  <br/> |IID_IXPLogon  <br/> |
|Tipo de ponteiro:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Retorna os tipos de destinatários que processa o provedor de transporte.  <br/> |
|**RegisterOptions** <br/> | *Não tem suporte ou documentadas.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Sinaliza a ocorrência de um evento sobre quais o provedor de transporte solicitado notificação.  <br/> |
|[Ocioso](ixplogon-idle.md) <br/> |Indica que o sistema está ocioso, permitindo que o provedor de transporte executar operações de baixa prioridade.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Inicia o processo de logoff.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indica que o MAPI spooler tem uma mensagem para o provedor de transporte fornecer.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informa o provedor de transporte que o MAPI spooler concluído seu processamento em uma mensagem de saída.  <br/> |
|[Votação](ixplogon-poll.md) <br/> |Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Inicia a transferência de uma mensagem de entrada do provedor de transporte para o spooler MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Abre o objeto de status do provedor de transporte.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Verifica o status de externo do provedor de transporte.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Solicita que o provedor de transporte imediatamente entrega todas as mensagens de entrada ou saídas pendentes.  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

