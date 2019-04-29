---
title: Carregar estado da mensagem
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
# <a name="upload-message-state"></a>Carregar estado da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de mensagem de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPMSG](upmsg.md)** <br/> |
|A partir deste Estado:  <br/> |[Carregar estado da tabela](upload-table-state.md) <br/> |
|Para este Estado:  <br/> |Carregar estado da tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia o carregamento de um item do Outlook (email, calendário, contato, tarefa, anotação ou diário) que é novo ou que foi movido para a pasta atual ou que foi modificado. O Outlook Inicializa a estrutura de dados do correpsonding **UPMSG** com as informações apropriadas para o item como sendo adicionado, movido ou modificado. 
  
Se o item tiver sido adicionado ou movido, o cliente adicionará ou atualizará o item, apropriadamente, no servidor. 
  
Se o item tiver sido modificado, o Outlook especificará ainda mais na estrutura de dados do **UPMSG** se as modificações estiverem em um cabeçalho de mensagem (caso em que o item é o cabeçalho da mensagem), nas propriedades do item ou no próprio item que requer conflito solução. O cliente atualiza o item no servidor. 
  
Quando o carregamento do item termina, o Outlook observa que a mensagem foi carregada, de forma que ela não seja processada em um carregamento subsequente. O repositório local retorna ao estado de carregamento da tabela.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

