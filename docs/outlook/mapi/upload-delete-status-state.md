---
title: Carregar estado de status de exclusão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357705"
---
# <a name="upload-delete-status-state"></a>Carregar estado de status de exclusão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de upload de status de exclusão da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPDEL](updel.md)** <br/> |
|A partir deste Estado:  <br/> |[Carregar estado da tabela](upload-table-state.md) <br/> |
|Para este Estado:  <br/> |Carregar estado da tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia a atualização em um servidor de itens do Outlook (email, calendário, contato, tarefa, anotação ou diário) que tenha sido excluído em uma pasta em um repositório local especificado em um estado de tabela de carregamento anterior. Durante esse Estado, o Outlook Inicializa membros na estrutura de dados do **UPDEL** associada com informações sobre os itens que foram excluídos ou movidos da pasta. 
  
O cliente, em seguida, exclui os itens especificados na pasta no servidor. Para diferenciar itens que foram movidos em vez de terem sido excluídos, o cliente deve verificar os membros *pupmov* identificados na estrutura **UPDEL** . 
  
Quando esse estado termina, o Outlook limpa as informações internas indicando que o item foi excluído; Consequentemente, o Outlook não terá mais um registro do item. O repositório local retorna ao estado de carregamento da tabela.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

