---
title: Estado Carregar Tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405818"
---
# <a name="upload-table-state"></a>Estado Carregar Tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado da tabela de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Desse estado:  <br/> |[Sincronizar o estado do conteúdo](synchronize-contents-state.md) <br/> |
|Para esse estado:  <br/> |[Carregar estado da mensagem,](upload-message-state.md) [carregar estado de status de exclusão,](upload-delete-status-state.md)carregar estado de status de [leitura](upload-read-status-state.md)ou sincronizar o estado do conteúdo  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia o carregamento do conteúdo de uma pasta que foi especificada em um estado de conteúdo de sincronização anterior. A pasta pode ser um email, calendário, contatos, tarefas, anotações ou pasta de diário. Durante esse estado, o Outlook cria uma lista de itens que foram adicionados, modificados, movidos, excluídos ou marcados como lidos e prepara as informações internas apropriadas para o estado de carregamento da mensagem correspondente, estado de status de exclusão de upload ou estado de status de leitura de carregamento.
  
Quando esse estado termina, o Outlook marca a pasta como tendo seu conteúdo sincronizado, para que o conteúdo não seja carregado novamente até que outra modificação seja feita. O armazenamento local retorna ao estado de sincronização do conteúdo.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

