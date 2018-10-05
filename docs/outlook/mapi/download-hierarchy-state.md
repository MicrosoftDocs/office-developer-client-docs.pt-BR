---
title: Baixar estado da hierarquia
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384854"
---
# <a name="download-hierarchy-state"></a>Baixar estado da hierarquia

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de hierarquia de download da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_DOWNLOAD_HIERARCHY** <br/> |
|Estrutura de dados relacionados:  <br/> |**[DNHIER](dnhier.md)** <br/> |
|Desse estado:  <br/> |[Sincronizar o estado](synchronize-state.md) <br/> |
|Com esse estado:  <br/> |Sincronizar o estado  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia o download de uma hierarquia de árvore de pastas de um servidor no repositório local. 
  
Outlook inicializa a estrutura de dados **DNHIER** associada com um ponteiro para a hierarquia. O cliente downloads da hierarquia e insere novas pastas ou modificações em pastas no armazenamento local. O processo de download adota sincronização de alteração Incremental do Microsoft Exchange (ICS). Para obter mais informações sobre ICS, consulte [ICS critérios de avaliação](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).
  
Quando for encerrada nesse estado, o armazenamento local retorna para o estado de sincronização.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

