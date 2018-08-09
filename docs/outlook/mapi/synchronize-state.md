---
title: Sincronizar o estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770567"
---
# <a name="synchronize-state"></a>Sincronizar o estado

  
  
**Aplica-se a**: Outlook 
  
 Este tópico descreve o que acontece durante o estado de sincronização da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC** <br/> |
|Estrutura de dados relacionados:  <br/> |**[SYNC](sync.md)** <br/> |
|Desse estado:  <br/> |[Estado ocioso](idle-state.md) <br/> |
|Com esse estado:  <br/> |[Baixe o estado de hierarquia](download-hierarchy-state.md), [sincronizar o estado de conteúdo](synchronize-contents-state.md), [carregar o estado de hierarquia](upload-hierarchy-state.md)ou estado ocioso  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia a sincronização. Um repositório local pode fazer a transição para um carregamento ou em um estado de download, a partir daqui. Por exemplo, um repositório local pode mover para o estado de hierarquia de carregar para carregar uma hierarquia de pastas no servidor, ou ele pode executar uma sincronização completa primeiro carregamento da hierarquia e, em seguida, baixando a hierarquia do servidor.
  
Durante esse estado, o Outlook inicializa a estrutura de dados de **sincronização** associada com o caminho para o repositório local, para que o Outlook vê modificações durante outros estados. 
  
O cliente define o [in] membros de **sincronização**, que informa ao Outlook como lidar com outros estados. Por exemplo, o cliente pode definir *ulFlags* **UPS_UPLOAD_ONLY** e **UPS_THESE_FOLDERS** e *pel* a uma lista de identificadores de entrada das pastas para informar ao Outlook que apenas essas pastas será carregado. Quando for encerrada nesse estado, o armazenamento local será revertido para o estado ocioso. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

