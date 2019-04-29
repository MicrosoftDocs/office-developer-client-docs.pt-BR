---
title: Baixar o estado do cabeçalho da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417116"
---
# <a name="download-message-header-state"></a>Baixar o estado do cabeçalho da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o status de cabeçalho da mensagem de download da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Estrutura de dados relacionada:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|A partir deste Estado:  <br/> |[Estado Ocioso](idle-state.md) <br/> |
|Para este Estado:  <br/> |Estado Ocioso  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Durante esse Estado, o cliente atualiza o cabeçalho de uma mensagem em um repositório local. O repositório local entra nesse estado no **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** e sai quando **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** é chamado. Durante esse Estado, o Outlook Inicializa membros da estrutura de dados do **HDRSYNC** associada com informações sobre o cabeçalho de uma mensagem. O cliente primeiro baixa o item de mensagem completo do servidor e, em seguida, atualiza o cabeçalho do item de mensagem localmente. 
  
Quando o sincronização termina, o cliente define os resultados do download. O repositório local retorna ao estado ocioso.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

