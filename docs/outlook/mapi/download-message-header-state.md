---
title: Baixar Estado do Header de Mensagem
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
# <a name="download-message-header-state"></a>Baixar Estado do Header de Mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado do header da mensagem de download da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Estrutura de dados relacionada:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Desse estado:  <br/> |[Estado Ocioso](idle-state.md) <br/> |
|Para esse estado:  <br/> |Estado Ocioso  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Durante esse estado, o cliente atualiza o header de uma mensagem em um armazenamento local. O armazenamento local entra nesse estado após **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** e sai quando **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** é chamado. Durante esse estado, o Outlook inicializa membros da estrutura de **dados HDRSYNC** associada com informações sobre o header de uma mensagem. O cliente primeiro baixa o item de mensagem completo do servidor e atualiza o título do item de mensagem localmente. 
  
Quando a sincronização termina, o cliente define os resultados de download. O armazenamento local retorna ao estado ocioso.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

