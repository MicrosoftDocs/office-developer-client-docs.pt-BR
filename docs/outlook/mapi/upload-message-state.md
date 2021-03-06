---
title: Estado carregar mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433798"
---
# <a name="upload-message-state"></a>Estado carregar mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado da mensagem de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|Desse estado:  <br/> |[Estado carregar tabela](upload-table-state.md) <br/> |
|Para esse estado:  <br/> |Estado carregar tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia o carregamento de um item do Outlook (email, calendário, contato, tarefa, anotação ou diário) que é novo ou foi movido para a pasta atual ou que foi modificado. Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified. 
  
Se o item tiver sido adicionado ou movido, o cliente adicionará ou atualizará adequadamente o item no servidor. 
  
Se o item tiver sido modificado, o Outlook especificará ainda mais na estrutura de dados **UPMSG** se as modificações estão em um header de mensagem (nesse caso, o item é o header da mensagem), nas propriedades do item ou no próprio item que exige resolução de conflitos. Em seguida, o cliente atualiza o item no servidor. 
  
Quando o carregamento do item termina, o Outlook observa que a mensagem foi carregada, para que ela não seja processada em um carregamento subsequente. O armazenamento local retorna ao estado da tabela de carregamento.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

