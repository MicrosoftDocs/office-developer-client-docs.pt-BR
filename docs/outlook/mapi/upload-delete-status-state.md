---
title: Carregar estado do status de exclusão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4a45cfafec5126c72f365858e41963bc95fa707a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574542"
---
# <a name="upload-delete-status-state"></a>Carregar estado do status de exclusão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado do carregamento excluir status da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Estrutura de dados relacionados:  <br/> |**[UPDEL](updel.md)** <br/> |
|Desse estado:  <br/> |[Carregar o estado da tabela](upload-table-state.md) <br/> |
|Com esse estado:  <br/> |Carregar o estado da tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia os itens do Outlook (email, calendário, contatos, tarefas, nota ou diário) que foram excluídos em uma pasta em um repositório local especificado em um estado de tabela anterior para carregar a atualização em um servidor. Durante esse estado, o Outlook inicializa membros na estrutura de dados **UPDEL** associada com informações para os itens que tenham sido excluído ou movido da pasta. 
  
Em seguida, o cliente exclui os itens especificados na pasta no servidor. Para distinguir os itens que foram movidos em vez de ter sido excluído, o cliente deve verificar os membros de *pupmov* identificados na estrutura **UPDEL** . 
  
Quando for encerrada nesse estado, o Outlook limpa as informações internas, indicando que o item foi excluído; Consequentemente, o Outlook não terá mais um registro do item. Armazenamento local retorna para o estado da tabela de carregamento.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

