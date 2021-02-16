---
title: IABLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon
api_type:
- COM
ms.assetid: fe340182-f41e-42e7-b8e8-cc005b1e9a5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fc8615fcd984623ae9c17c45fb7b51a4498a723b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431075"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Acessa recursos em um provedor de agendamento de endereços.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Exposto por:  <br/> |Objetos de logon do livro de endereços  <br/> |
|Implementado por:  <br/> |Provedores de lista de endereços  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IABLogon  <br/> |
|Tipo de ponteiro:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro do provedor de agendas anterior.  <br/> |
|[Fazer logoff](iablogon-logoff.md) <br/> |Inicia o processo de logoff.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Advise](iablogon-advise.md) <br/> |Registra o chamador para receber notificação de eventos especificados que afetam um contêiner, um usuário de mensagens ou uma lista de distribuição.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Cancela notificações que foram configuradas anteriormente com uma chamada para o **método Advise.**  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Abre o objeto de status do provedor.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Abre uma entrada de destinatário que tem dados residindo em um provedor de agendamento de endereço de host.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Retorna uma tabela de modelos one-off para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter informações gerais sobre os métodos da interface **IABLogon,** consulte Implementando o [logon do provedor de serviços.](implementing-service-provider-logon.md)
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

