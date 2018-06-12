---
title: Estado do download tabela
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 6a29cc131b4fe352b067e343376b2b705e8e3244
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766465"
---
# <a name="download-table-state"></a>Estado do download tabela

  
  
**Aplica-se a**: Outlook 
  
 Este tópico descreve o que acontece durante o estado da tabela de download da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_DOWNLOAD_TABLE** <br/> |
|Estrutura de dados relacionados:  <br/> |**[DNTBL](dntbl.md)** <br/> |
|Desse estado:  <br/> |[Sincronizar o estado de conteúdo](synchronize-contents-state.md) <br/> |
|Com esse estado:  <br/> |Sincronizar o estado de conteúdo  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia baixando uma pasta. Durante esse estado, o Outlook inicializa a estrutura de dados **DNTBL** associada com informações sobre a pasta. O cliente baixa o conteúdo da pasta e atualiza a pasta no armazenamento local com conteúdo novo, modificações ou exclusões do servidor. O processo de download adota sincronização de alteração Incremental do Microsoft Exchange (ICS). Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).
  
Quando for encerrada nesse estado, o armazenamento local retorna ao estado sincronizar conteúdo.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

