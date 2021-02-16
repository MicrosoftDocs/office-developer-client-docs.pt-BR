---
title: Estado de Hierarquia de Carregamento
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39c4198-4913-5e86-900a-32e5ba5d801c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f789f4d7bbaf585d0d80f2208c35313542dfc191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415422"
---
# <a name="upload-hierarchy-state"></a>Estado de Hierarquia de Carregamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de hierarquia de carregamento da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_HIERARCHY** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPHIER](uphier.md)** <br/> |
|Desse estado:  <br/> |[Estado Sincronizar](synchronize-state.md) <br/> |
|Para esse estado:  <br/> |[Estado carregar pasta](upload-folder-state.md)ou sincronizar estado  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que parte de um estado para outro deve eventualmente retornar ao primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia o carregamento de uma hierarquia de árvore de pastas que foi especificada em um estado de sincronização anterior. Outlook determines the number of folders that have been created or modified in that hierarchy and initializes  *cEnt*  in **UPHIER**. O Outlook também mantém uma contagem do número de pastas carregadas com outro  *membro iEnt*  . Para carregar cada uma das  *pastas cEnt,*  o cliente move o armazenamento local para o estado da pasta de carregamento, retornando ao estado de hierarquia de carregamento quando o carregamento da pasta é finaliza. 
  
Quando o estado de hierarquia de upload termina, o armazenamento local retorna ao estado de sincronização.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

