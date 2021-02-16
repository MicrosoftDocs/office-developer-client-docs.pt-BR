---
title: IMSLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon
api_type:
- COM
ms.assetid: d87093dc-f705-465f-ab3c-944ca0cd3e54
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 991e48aa458a58ad2d7d688e81dbb357ef9bda5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428876"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Acessa recursos em um objeto de logon do armazenamento de mensagens.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Exposto por:  <br/> |Objetos de logon do armazenamento de mensagens  <br/> |
|Implementado por:  <br/> |Provedores de armazenamento de mensagens  <br/> |
|Chamado por:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMSLogon  <br/> |
|Tipo de ponteiro:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de armazenamento de mensagens.  <br/> |
|[Fazer logoff](imslogon-logoff.md) <br/> |Faz o login de um provedor de armazenamento de mensagens.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Abre uma pasta ou objeto message e retorna um ponteiro para o objeto para fornecer mais acesso.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Advise](imslogon-advise.md) <br/> |Registra um objeto com um provedor de armazenamento de mensagens para notificações sobre alterações no armazenamento de mensagens.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Remove o registro de um objeto para notificação de alterações do armazenamento de mensagens estabelecidas anteriormente usando uma chamada para o **método IMSLogon::Advise.**  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Abre um objeto de status.  <br/> |
   
## <a name="remarks"></a>Comentários

O objeto de logon do armazenamento de mensagens é a parte de um provedor de armazenamento de mensagens aberto que o MAPI chama diretamente. Há uma correspondência um-para-um entre o objeto de logon do armazenamento de mensagens que o MAPI chama e o objeto de armazenamento de mensagens que os aplicativos cliente chamam; você pode pensar no logon e armazenar objetos como um objeto que expõe duas interfaces. Os dois objetos são criados juntos e liberados juntos.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

