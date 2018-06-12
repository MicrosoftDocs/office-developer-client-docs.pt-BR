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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7419a0df7a2f3b76caeeb1ca564624d437eddd52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767604"
---
# <a name="iostx--iunknown"></a>IOSTX: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Fornece os métodos de sincronização. Essa interface recupera as informações necessárias para replicar alterações locais para o servidor e as alterações no repositório local no servidor.
  
|||
|:-----|:-----|
|Provided by:  <br/> |[IPSTX::GetSyncObject](iostx-setsyncresult.md) <br/> |
|Identificador de interface:  <br/> |IID_IOSTX  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[GetLastError](iostx-getlasterror.md) <br/> |Obtém informações estendidas sobre o último erro.  <br/> |
|[InitSync](iostx-initsync.md) <br/> |Informa o armazenamento local que sincronização está prestes a iniciar.  <br/> |
|[SyncBeg](iostx-syncbeg.md) <br/> |Prepara o armazenamento local para sincronização em um estado particular e recupera as informações necessárias para replicar.  <br/> |
|[SyncEnd](iostx-syncend.md) <br/> |Finaliza a sincronização no estado atual e sai desse estado.  <br/> |
|[SyncHdrBeg](iostx-synchdrbeg.md) <br/> |Inicia a sincronização de um cabeçalho de mensagem.  <br/> |
|[SyncHdrEnd](iostx-synchdrend.md) <br/> |Finaliza a sincronização para um cabeçalho de mensagem.  <br/> |
|[SetSyncResult](iostx-setsyncresult.md) <br/> |Define o resultado da sincronização.  <br/> |
| *Membro do espaço reservado*  <br/> | *Não tem suporte ou documentadas.*  <br/> |
   
## <a name="remarks"></a>Coment�rios

Quando um cliente carrega ou sincroniza pastas e o conteúdo da pasta em um repositório local, ele transfere o armazenamento local de um estado para outro conforme ilustrado no diagrama a transição de estado no [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md). Este é a ordem de eventos para o cliente mover o repositório local de um estado para outro:
  
1. O cliente chama **IOSTX::InitSync** para informar o armazenamento local que a replicação está prestes a iniciar. 
    
2. Dependendo da direção da replicação e os objetos para replicar, o cliente chama **IOSTX::SyncBeg** para começar a replicação em um estado apropriado. O Outlook oferece o cliente as informações necessárias e o cliente executa a replicação. 
    
3. O cliente chama **IOSTX::SetSyncResult** para retornar o resultado da replicação. 
    
4. O cliente chama **IOSTX::SyncEnd** para encerrar a replicação, fornecendo Outlook as informações necessárias para replicação subsequentes. 
    
Em particular, ao fazer o download de itens de mensagem, o cliente usa **IOSTX::SyncHdrBeg** e **IOSTX::SyncHdrEnd** para atualizar um item de mensagem completo com o cabeçalho da mensagem no armazenamento local: 
  
1. Após a **IOSTX::SyncHdrBeg**, o local armazenar transições para o estado de cabeçalho de mensagem do download. Inicialmente, o Outlook fornece ao cliente com o cabeçalho da mensagem atual no armazenamento local.
    
2. O cliente baixa um item de mensagem completa em conjunto com o cabeçalho da mensagem.
    
3. Outlook atualiza o item no armazenamento local com o item de mensagem completa.
    
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)

