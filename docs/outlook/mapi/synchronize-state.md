---
title: Estado de Sincronização
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
# <a name="synchronize-state"></a>Estado de Sincronização

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de sincronização da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC** <br/> |
|Estrutura de dados relacionada:  <br/> |**[SYNC](sync.md)** <br/> |
|Desse estado:  <br/> |[Estado Ocioso](idle-state.md) <br/> |
|Para esse estado:  <br/> |[Estado de hierarquia de download,](download-hierarchy-state.md) [estado de sincronização de conteúdo,](synchronize-contents-state.md)estado [de hierarquia de carregamento](upload-hierarchy-state.md)ou estado ocioso  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia a sincronização. Um armazenamento local pode fazer a transição para um estado de upload ou download a partir daqui. Por exemplo, um armazenamento local pode mover para o estado de hierarquia de carregamento para carregar uma hierarquia de pastas para o servidor ou pode executar uma sincronização completa carregando primeiro a hierarquia e, em seguida, baixando a hierarquia do servidor.
  
Durante esse estado, o Outlook inicializa a estrutura de dados **SYNC** associada com o caminho para o armazenamento local, para que o Outlook veja modificações durante outros estados. 
  
O cliente define os membros [in] de **SYNC**, que informa ao Outlook como lidar com outros estados. Por exemplo, o cliente pode definir  *ulFlags*  como **UPS_UPLOAD_ONLY** e **UPS_THESE_FOLDERS** e  *pel*  para uma lista de identificadores de entrada das pastas para dizer ao Outlook que somente essas pastas serão carregadas. Quando esse estado termina, o armazenamento local reverte para o estado ocioso. 
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

