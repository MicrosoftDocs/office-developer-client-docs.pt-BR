---
title: Carregar estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342837"
---
# <a name="upload-table-state"></a>Carregar estado da tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de carregamento da tabela da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|A partir deste Estado:  <br/> |[Sincronizar o estado do conteúdo](synchronize-contents-state.md) <br/> |
|Para este Estado:  <br/> |[Carregar estado da mensagem](upload-message-state.md), [carregar estado de status de exclusão](upload-delete-status-state.md), carregar o estado de status de [leitura](upload-read-status-state.md)ou sincronizar o estado do conteúdo  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia o carregamento do conteúdo de uma pasta que foi especificada em um estado de sincronização anterior do conteúdo. A pasta pode ser uma pasta de email, calendário, contatos, tarefas, anotações ou diário. Durante esse Estado, o Outlook cria uma lista de itens que foram adicionados, modificados, movidos, excluídos ou marcados como lidos e prepara as informações internas apropriadas para o estado de mensagem de carregamento correspondente, carregar o estado de status de exclusão ou carregar o status de leitura Estado.
  
Quando esse estado termina, o Outlook marca a pasta como tendo seu conteúdo sincronizado, para que o conteúdo não seja carregado novamente até que outra modificação seja feita. O repositório local retorna ao estado sincronizar conteúdo.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

