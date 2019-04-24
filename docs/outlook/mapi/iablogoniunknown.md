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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348829"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Acessa recursos em um provedor de catálogo de endereços.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Exposto por:  <br/> |Objetos de logon do catálogo de endereços  <br/> |
|Implementado por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IABLogon  <br/> |
|Tipo de ponteiro:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior do provedor de catálogo de endereços.  <br/> |
|[Fazer logoff](iablogon-logoff.md) <br/> |Inicia o processo de logoff.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer acesso adicional.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Utilizar](iablogon-advise.md) <br/> |Registra o chamador para receber notificações de eventos específicos que afetam um contêiner, usuário de mensagens ou lista de distribuição.  <br/> |
|[Cancelar](iablogon-unadvise.md) <br/> |Cancela as notificações que foram configuradas anteriormente com uma chamada para o método **Advise** .  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Abre o objeto status do provedor.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Abre uma entrada de destinatário que tem dados residindo em um provedor de catálogo de endereços de host.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Retorna uma tabela de modelos únicos para a criação de destinatários a serem adicionados à lista de destinatários de uma mensagem de saída.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter informações gerais sobre os métodos da interface **IABLogon** , consulte [Implementing Service Provider logon](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

