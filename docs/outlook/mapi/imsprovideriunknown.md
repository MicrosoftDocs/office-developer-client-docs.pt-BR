---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412860"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a um provedor de repositório de mensagens por meio de um objeto do provedor de repositório de mensagens. Este objeto do provedor de repositório de mensagens é retornado no logon do provedor pela função de ponto de entrada do provedor do repositório de mensagens [MSProviderInit](msproviderinit.md) . O objeto do provedor de repositório de mensagens é usado principalmente por aplicativos cliente e o spooler MAPI para abrir repositórios de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Exposto por:  <br/> |Objetos do provedor do repositório de mensagens  <br/> |
|Implementado por:  <br/> |Provedores de repositórios de mensagens  <br/> |
|Chamado por:  <br/> |MAPI e o spooler MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMSProvider  <br/> |
|Tipo de ponteiro:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Fecha um provedor de repositório de mensagens de maneira ordenada.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Registra o MAPI em uma instância de um provedor de armazenamento de mensagens.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Registra o spooler MAPI em um repositório de mensagens.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compara dois identificadores de entrada de repositório de mensagens para determinar se eles se referem ao mesmo objeto Store.  <br/> |
   
## <a name="remarks"></a>Comentários

O MAPI usa um objeto de provedor de repositório de mensagens por sessão, independentemente de quantas lojas de mensagens são abertas pelo provedor da loja. Se uma segunda sessão MAPI fizer logon em qualquer repositório aberto, as chamadas MAPI **MSProviderInit** uma segunda vez para criar um novo objeto do provedor de repositório de mensagens para essa sessão usar. 
  
Um objeto do provedor de repositório de mensagens deve conter o seguinte para funcionar corretamente:
  
- Um ponteiro de rotina de alocação de memória do _lpMalloc_ para uso por todos os repositórios abertos usando este objeto de provedor. 
    
- Os ponteiros de rotina _lpfAllocateBuffer_, _ lpfAllocateMore _ e _lpfFreeBuffer_ para as funções de alocação de memória [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Uma lista vinculada de todos os repositórios abertos usando este objeto de provedor e ainda não foi fechado.
    
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

