---
title: Carregar o estado da hierarquia
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ed24682086556addf76b8451674a73bd82ce050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572183"
---
# <a name="upload-hierarchy-state"></a>Carregar o estado da hierarquia

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de hierarquia de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Estrutura de dados relacionados:  <br/> |**[UPHIER](uphier.md)** <br/> |
|Desse estado:  <br/> |[Sincronizar o estado](synchronize-state.md) <br/> |
|Com esse estado:  <br/> |[Carregar o estado de pasta](upload-folder-state.md), ou sincronizar o estado  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente de um estado de início para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia o carregamento de uma hierarquia de árvore de pastas que foi especificada na precedidos sincronizar o estado. O Outlook determina o número de pastas que foram criados ou modificados nessa hierarquia e inicializa *cEnt* em **UPHIER**. Além disso, o Outlook mantém uma contagem do número de pastas carregados com *iEnt* de outro membro. Para carregar a cada uma das pastas *cEnt* , o cliente move o armazenamento local para o estado da pasta de carregamento, retornando para o estado de hierarquia de carregamento quando termina o carregamento da pasta. 
  
Quando o estado de hierarquia de carregamento for encerrada, armazenamento local retorna ao estado sincronizar.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

