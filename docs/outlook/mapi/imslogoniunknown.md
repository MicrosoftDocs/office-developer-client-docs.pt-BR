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
ms.openlocfilehash: 013903f36bf648c4aed194c88104e7dd981b199f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563937"
---
# <a name="imslogon--iunknown"></a>IMSLogon : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recursos de acessos em uma mensagem armazenam o objeto de logon.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Expostos pelo:  <br/> |Objetos de logon do repositório de mensagem  <br/> |
|Implementada por:  <br/> |Provedores de armazenamento de mensagem  <br/> |
|Chamado pelo:  <br/> |MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMSLogon  <br/> |
|Tipo de ponteiro:  <br/> |LPMSLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](imslogon-getlasterror.md) <br/> |Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para o objeto de repositório de mensagem.  <br/> |
|[Fazer logoff](imslogon-logoff.md) <br/> |Logs de uma mensagem armazenam provedor.  <br/> |
|[OpenEntry](imslogon-openentry.md) <br/> |Abre uma pasta ou um objeto de mensagem e retorna um ponteiro para o objeto para fornecer mais acesso.  <br/> |
|[CompareEntryIDs](imslogon-compareentryids.md) <br/> |Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.  <br/> |
|[Aviso](imslogon-advise.md) <br/> |Registra um objeto com um provedor de armazenamento de mensagem para notificações sobre alterações no armazenamento de mensagens.  <br/> |
|[Unadvise](imslogon-unadvise.md) <br/> |Remove o registro de um objeto de notificação de alteração de repositório de mensagem tenha estabelecido por meio de uma chamada ao método **IMSLogon::Advise** .  <br/> |
|[OpenStatusEntry](imslogon-openstatusentry.md) <br/> |Abre um objeto de status.  <br/> |
   
## <a name="remarks"></a>Comentários

O objeto de logon do repositório de mensagens é a parte de um provedor de armazenamento de mensagem aberta diretamente chamadas de MAPI. Não há uma correspondência direta entre o objeto de logon de armazenamento de mensagem que armazenam o objeto que aplicativos de cliente chamam; chamadas MAPI e a mensagem Você pode imaginar o logon e armazenar objetos como um único objeto que expõe duas interfaces. Os dois objetos são criados juntos e liberação juntos.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

