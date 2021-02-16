---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431992"
---
# <a name="iostx--iunknown"></a>IOSTX : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece métodos de sincronização. Essa interface recupera as informações necessárias para replicar as alterações locais no servidor e nas alterações do servidor no armazenamento local.
  
|||
|:-----|:-----|
|Provided by:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificador de interface:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Obtém informações estendidas sobre o último erro.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informa ao armazenamento local que a sincronização está prestes a iniciar.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prepara o armazenamento local para sincronização em um estado específico e recupera as informações necessárias para replicar.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Encerra a sincronização no estado atual e sai desse estado.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Inicia a sincronização para um header de mensagem.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Encerra a sincronização para um header de mensagem.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Define o resultado da sincronização.  <br/> |
| *Membro placeholder*  <br/> | *Sem suporte ou documentado.*  <br/> |
   
## <a name="remarks"></a>Comentários

Quando um cliente carrega ou sincroniza pastas e conteúdo de pastas em um armazenamento local, ele move o armazenamento local de um estado para outro, conforme ilustrado no diagrama de transição de estado em [Sobre](about-the-replication-state-machine.md)a Máquina de Estado de Replicação. A seguir está a ordem dos eventos para o cliente mover o armazenamento local de um estado para outro:
  
1. O cliente chama **IOSTX::InitSync** para informar ao armazenamento local que a replicação está prestes a iniciar. 
    
2. Dependendo da direção da replicação e dos objetos a replicar, o cliente chama **IOSTX::SyncBeg** para iniciar a replicação no estado apropriado. O Outlook fornece ao cliente as informações necessárias, e o cliente executa a replicação. 
    
3. O cliente chama **IOSTX::SetSyncResult** para retornar o resultado da replicação. 
    
4. O cliente chama **IOSTX::SyncEnd** para encerrar a replicação, fornecendo ao Outlook as informações necessárias para a replicação subsequente. 
    
Em particular, ao baixar itens de mensagem, o cliente usa **IOSTX::SyncHdrBeg** e **IOSTX::SyncHdrEnd** para atualizar um item de mensagem completo com o header da mensagem no armazenamento local: 
  
1. Em **IOSTX::SyncHdrBeg**, o armazenamento local faz a transição para o estado do header da mensagem de download. Inicialmente, o Outlook fornece ao cliente o header de mensagem atual no armazenamento local.
    
2. O cliente baixa um item de mensagem completo junto com o header da mensagem.
    
3. O Outlook atualiza o item no armazenamento local com o item de mensagem completo.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes de MAPI](mapi-constants.md)

