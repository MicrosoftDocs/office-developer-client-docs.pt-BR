---
title: Estado de Hierarquia de Download
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337006"
---
# <a name="download-hierarchy-state"></a>Estado de Hierarquia de Download

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de hierarquia de download da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Estrutura de dados relacionada:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Desse estado:  <br/> |[Estado Sincronizar](synchronize-state.md) <br/> |
|Para esse estado:  <br/> |Estado Sincronizar  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia o download de uma hierarquia de árvore de pastas de um servidor para o armazenamento local. 
  
O Outlook inicializa a estrutura de dados **DNHIER** associada com um ponteiro para a hierarquia. O cliente baixa a hierarquia e insere novas pastas ou modificações em pastas no armazenamento local. O processo de download adota o Microsoft Exchange Incremental Change Synchronization (ICS). Confira mais informações sobre ICS em [Critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Quando esse estado termina, o armazenamento local retorna ao estado de sincronização.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

