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
ms.openlocfilehash: 784430f1286c9a017337a0fae4b269757a56a3e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766860"
---
# <a name="iablogon--iunknown"></a>IABLogon : IUnknown

  
  
**Aplica-se a**: Outlook 
  
Recursos de acessos em um provedor de catálogo de endereços.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Expostos pelo:  <br/> |Objetos de logon do catálogo de endereços  <br/> |
|Implementada por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IABLogon  <br/> |
|Tipo de ponteiro:  <br/> |LPABLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](iablogon-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro de provedor de catálogo de endereços anterior.  <br/> |
|[Fazer logoff](iablogon-logoff.md) <br/> |Inicia o processo de logoff.  <br/> |
|[OpenEntry](iablogon-openentry.md) <br/> |Abre um contêiner, o usuário ou lista de distribuição de mensagens e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.  <br/> |
|[CompareEntryIDs](iablogon-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Aviso](iablogon-advise.md) <br/> |Registra o chamador para receber notificações de eventos especificados que afetam um contêiner, o usuário ou lista de distribuição de mensagens.  <br/> |
|[Unadvise](iablogon-unadvise.md) <br/> |Cancela notificações que foram definidas com uma chamada ao método **Advise** anteriormente.  <br/> |
|[OpenStatusEntry](iablogon-openstatusentry.md) <br/> |Abre o objeto de status do provedor.  <br/> |
|[OpenTemplateID](iablogon-opentemplateid.md) <br/> |Abre uma entrada do destinatário que possui dados que residem em um provedor de catálogo de endereço de host.  <br/> |
|[GetOneOffTable](iablogon-getoneofftable.md) <br/> |Retorna uma tabela de modelos únicos para a criação de destinatários a ser adicionado à lista de destinatários de uma mensagem de saída.  <br/> |
|[PrepareRecips](iablogon-preparerecips.md) <br/> |Prepara uma lista de destinatários para uso posterior pelo sistema de mensagens.  <br/> |
   
## <a name="remarks"></a>Comentários

Para obter informações gerais sobre os métodos da interface **IABLogon** , consulte [Implementando Logon do provedor de serviço](implementing-service-provider-logon.md).
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

