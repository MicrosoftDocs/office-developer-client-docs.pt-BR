---
title: Carregar Estado de Status de Exclusão
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dee566ad-b46d-1015-4b0b-6c3313060142
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dda9d23a572446a5fa79a9500eb69558b6e0debd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425838"
---
# <a name="upload-delete-status-state"></a>Carregar Estado de Status de Exclusão

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de status de exclusão de upload da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_DEL** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPDEL](updel.md)** <br/> |
|Desse estado:  <br/> |[Estado carregar tabela](upload-table-state.md) <br/> |
|Para esse estado:  <br/> |Estado carregar tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia a atualização em um servidor desses itens do Outlook (email, calendário, contato, tarefa, anotação ou diário) que foram excluídos em uma pasta em um armazenamento local especificado em um estado de tabela de carregamento anterior. Durante esse estado, o Outlook inicializa membros na estrutura de dados **UPDEL** associada com informações para os itens que foram excluídos ou movidos da pasta. 
  
Em seguida, o cliente exclui os itens especificados na pasta no servidor. Para distinguir os itens que foram movidos, em vez de terem sido excluídos, o cliente deve verificar os membros de *therunmov* identificados na estrutura **UPDEL.** 
  
Quando esse estado termina, o Outlook limpa as informações internas indicando que o item foi excluído; consequentemente, o Outlook não terá mais um registro do item. O armazenamento local retorna ao estado da tabela de carregamento.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

