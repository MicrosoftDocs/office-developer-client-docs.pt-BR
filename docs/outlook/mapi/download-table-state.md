---
title: Baixar o estado da tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338336"
---
# <a name="download-table-state"></a>Baixar o estado da tabela

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de download da tabela da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Estrutura de dados relacionada:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|A partir deste Estado:  <br/> |[Sincronizar o estado do conteúdo](synchronize-contents-state.md) <br/> |
|Para este Estado:  <br/> |Sincronizar o estado do conteúdo  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia o download de uma pasta. Durante esse Estado, o Outlook Inicializa a estrutura de dados **DNTBL** associada com informações sobre a pasta. O cliente baixa o conteúdo da pasta e atualiza a pasta no repositório local com novos conteúdos, modificações ou exclusões do servidor. O processo de download adota a sincronização de alteração incremental (ICS) do Microsoft Exchange. Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Quando esse estado termina, o repositório local retorna ao estado sincronizar conteúdo.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

