---
title: Carregar o estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bd54c30e8701a13637235e28ddcfef4c21d10a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576978"
---
# <a name="upload-table-state"></a>Carregar o estado da tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado da tabela de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_UPLOAD_TABLE** <br/> |
|Estrutura de dados relacionados:  <br/> |**[UPTBL](uptbl.md)** <br/> |
|Desse estado:  <br/> |[Sincronizar o estado de conteúdo](synchronize-contents-state.md) <br/> |
|Com esse estado:  <br/> |[Carregar o estado da mensagem](upload-message-state.md), [carregamento excluir estado de status](upload-delete-status-state.md), [carregamento ler o estado de status](upload-read-status-state.md), ou sincronizar o estado de conteúdo  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia carregar o conteúdo de uma pasta que foi especificado em um estado de conteúdo anterior sincronizar. A pasta pode ser uma pasta de email, calendário, contatos, tarefas, anotações ou diário. Durante esse estado, Outlook cria uma lista de itens que foram adicionados, modificado, movido, excluído ou marcado como lido e prepara as informações apropriadas de internas para o estado de mensagem de carregamento correspondente, carregar o estado de status de excluir ou carregar o status de leitura estado.
  
Quando for encerrada nesse estado, o Outlook marca a pasta como tendo seu conteúdo sincronizado, para que o conteúdo não será carregado novamente até que a outra modificação for feita. Armazenamento local retorna ao estado sincronizar conteúdo.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

