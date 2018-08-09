---
title: Baixar o estado do cabeçalho da mensagem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766443"
---
# <a name="download-message-header-state"></a>Baixar o estado do cabeçalho da mensagem

  
  
**Aplica-se a**: Outlook 
  
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

