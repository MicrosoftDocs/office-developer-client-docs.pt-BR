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
  
Fornece acesso a um provedor de armazenamento de mensagens por meio de um objeto de provedor de armazenamento de mensagens. Esse objeto do provedor de armazenamento de mensagens é retornado no logon do provedor pela função de ponto de entrada [MSProviderInit](msproviderinit.md) do provedor de armazenamento de mensagens. O objeto do provedor de armazenamento de mensagens é usado principalmente por aplicativos cliente e pelo spooler MAPI para abrir os armazenamentos de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Exposto por:  <br/> |Objetos do provedor do repositório de mensagens  <br/> |
|Implementado por:  <br/> |Provedores de armazenamento de mensagens  <br/> |
|Chamado por:  <br/> |MAPI and the MAPI spooler  <br/> |
|Identificador de interface:  <br/> |IID_IMSProvider  <br/> |
|Tipo de ponteiro:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Break](imsprovider-shutdown.md) <br/> |Fecha um provedor de armazenamento de mensagens de forma pedido.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Registra MAPI em uma instância de um provedor de armazenamento de mensagens.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Registra o spooler MAPI em um armazenamento de mensagens.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compara dois identificadores de entrada do armazenamento de mensagens para determinar se eles se referem ao mesmo objeto de armazenamento.  <br/> |
   
## <a name="remarks"></a>Comentários

O MAPI usa um objeto de provedor de armazenamento de mensagens por sessão, independentemente de quantos armazenamentos de mensagens sejam abertos pelo provedor de armazenamento. Se uma segunda sessão MAPI faz o login em qualquer armazenamento aberto, o MAPI chama **MSProviderInit** uma segunda vez para criar um novo objeto de provedor de armazenamento de mensagens para essa sessão usar. 
  
Um objeto de provedor de armazenamento de mensagens deve conter o seguinte para funcionar corretamente:
  
- Um ponteiro de rotina de alocação de memória  _lpMalloc_ para uso por todos os armazenamentos abertos usando esse objeto de provedor. 
    
- The  _lpfAllocateBuffer_, _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions. 
    
- Uma lista vinculada de todos os armazenamentos abertos usando esse objeto provedor e ainda não fechado.
    
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

