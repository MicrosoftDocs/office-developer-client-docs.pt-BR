---
title: Sincronizar estado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414624"
---
# <a name="synchronize-state"></a>Sincronizar estado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de sincronização da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC** <br/> |
|Estrutura de dados relacionada:  <br/> |**[SINCRONIZAÇÃO](sync.md)** <br/> |
|A partir deste Estado:  <br/> |[Estado Ocioso](idle-state.md) <br/> |
|Para este Estado:  <br/> |[Estado de hierarquia de download](download-hierarchy-state.md), sincronizar estado do [conteúdo](synchronize-contents-state.md), estado da [hierarquia de carregamento](upload-hierarchy-state.md)ou estado ocioso  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia a sincronização. Um repositório local pode fazer a transição para um upload ou um estado de download a partir daqui. Por exemplo, um repositório local pode ser movido para o estado de hierarquia de upload para carregar uma hierarquia de pastas para o servidor ou pode executar uma sincronização completa carregando primeiro a hierarquia e, em seguida, baixando a hierarquia do servidor.
  
Durante esse Estado, o Outlook Inicializa a estrutura de dados de **sincronização** associada com o caminho para o repositório local, para que o Outlook Veja modificações durante outros Estados. 
  
O cliente define os membros [in] de **Sync**, que dizem ao Outlook como lidar com outros Estados. Por exemplo, o cliente pode definir *parâmetroulflags* como **UPS_UPLOAD_ONLY** e **UPS_THESE_FOLDERS** e *PEL* como uma lista de identificadores de entrada das pastas para informar ao Outlook que somente essas pastas serão carregadas. Quando esse estado termina, o repositório local reverte para o estado ocioso. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

