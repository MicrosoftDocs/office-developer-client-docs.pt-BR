---
title: Carregar o estado das mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575410"
---
# <a name="upload-message-state"></a>Carregar o estado das mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de mensagem de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Estrutura de dados relacionados:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Desse estado:  <br/> |[Carregar o estado da tabela](upload-table-state.md) <br/> |
|Com esse estado:  <br/> |Carregar o estado da tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia o carregamento de um item do Outlook (email, calendário, contatos, tarefas, nota ou diário) que há de novo ou foi movida para a pasta atual ou que tenha sido modificado. Outlook inicializa a estrutura de dados **UPMSG** correpsonding com as informações apropriadas para o item, como sendo adicionado, movido ou modificado. 
  
Se o item foi adicionado ou movido, o cliente, em seguida, apropriadamente adiciona ou atualiza o item no servidor. 
  
Se o item tiver sido modificado, Outlook ainda mais especifica na estrutura de dados **UPMSG** se as modificações estão em um cabeçalho de mensagem (caso em que o item é o cabeçalho da mensagem), nas propriedades do item ou no próprio item que requer o conflito resolução. O cliente, em seguida, atualiza o item no servidor. 
  
Quando o carregamento do item for encerrada, Outlook notas que a mensagem foi carregada, para que ele não será processado em um carregamento subsequente. Armazenamento local retorna para o estado da tabela de carregamento.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

