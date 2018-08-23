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
ms.openlocfilehash: 1c00e54d02ba494c94c9826eabe142e1bd3b9a80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579624"
---
# <a name="imsprovider--iunknown"></a>IMSProvider : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a um provedor de armazenamento de mensagens por meio de um objeto de provedor de armazenamento de mensagem. Este objeto de provedor de armazenamento de mensagens é retornado no logon do provedor por função de ponto de entrada do provedor de repositório a mensagem [MSProviderInit](msproviderinit.md) . O objeto de provedor de armazenamento de mensagem é usado principalmente pelos aplicativos cliente e o MAPI spooler para abrir armazenamentos de mensagem. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Expostos pelo:  <br/> |Objetos do provedor de repositório de mensagem  <br/> |
|Implementada por:  <br/> |Provedores de armazenamento de mensagem  <br/> |
|Chamado pelo:  <br/> |O MAPI spooler e MAPI  <br/> |
|Identificador de interface:  <br/> |IID_IMSProvider  <br/> |
|Tipo de ponteiro:  <br/> |LPMSPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Shutdown](imsprovider-shutdown.md) <br/> |Fecha um provedor de armazenamento de mensagem de forma ordenada.  <br/> |
|[Logon](imsprovider-logon.md) <br/> |Logs de MAPI em uma instância de um provedor de armazenamento de mensagem.  <br/> |
|[SpoolerLogon](imsprovider-spoolerlogon.md) <br/> |Registra o MAPI spooler em um armazenamento de mensagens.  <br/> |
|[CompareStoreIDs](imsprovider-comparestoreids.md) <br/> |Compara dois mensagem repositório identificadores de entrada para determinar se eles se referem ao mesmo objeto store.  <br/> |
   
## <a name="remarks"></a>Comentários

O MAPI usa um objeto de provedor de armazenamento de mensagens por sessão, não importa quantos mensagem repositórios abertos pelo provedor de armazenamento. Se um segundo MAPI sessão faz logon em qualquer repositórios open, chamadas MAPI **MSProviderInit** uma segunda vez para criar um novo objeto de provedor de repositório de mensagem para a sessão de usar. 
  
Um objeto de provedor de armazenamento de mensagem deve conter o seguinte para que funcionem corretamente:
  
- Um _lpMalloc_ alocação de memória rotina ponteiro para uso por todos os repositórios aberta usando o objeto este provedor. 
    
- O _lpfAllocateBuffer_, _ lpfAllocateMore _ e ponteiros de rotina _lpfFreeBuffer_ às funções de alocação de memória [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) . 
    
- Uma lista vinculada de todos os repositórios aberta usando este objeto de provedor e ainda não foi fechado.
    
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

