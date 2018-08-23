---
title: Baixar o estado do cabeçalho da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c9d1745d25e7f7a5052d767350ade6723067d1b8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578840"
---
# <a name="download-message-header-state"></a>Baixar o estado do cabeçalho da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de cabeçalho de mensagem de download da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_DOWNLOAD_HEADER** <br/> |
|Estrutura de dados relacionados:  <br/> |**[HDRSYNC](hdrsync.md)** <br/> |
|Desse estado:  <br/> |[Estado ocioso](idle-state.md) <br/> |
|Com esse estado:  <br/> |Estado ocioso  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Durante esse estado, o cliente atualiza o cabeçalho de uma mensagem em um repositório local. Armazenamento local entra neste estado após **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** e sai quando **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** é chamado. Durante esse estado, o Outlook inicializa membros da estrutura de dados **HDRSYNC** associada com informações sobre o cabeçalho de uma mensagem. O cliente primeiramente baixa o item de mensagem completa do servidor e atualiza o cabeçalho do item mensagem localmente. 
  
Quando a sincronização for encerrada, o cliente define os resultados de download. Armazenamento local retorna ao estado ocioso.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

