---
title: Sincronizar o estado do conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349564"
---
# <a name="synchronize-contents-state"></a>Sincronizar o estado do conteúdo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado sincronizar conteúdo da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Estrutura de dados relacionada:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|A partir deste Estado:  <br/> |[Estado Sincronizar](synchronize-state.md) <br/> |
|Para este Estado:  <br/> |[Baixar o estado da tabela](download-table-state.md), carregar o estado da [tabela](upload-table-state.md)ou sincronizar estado  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia um dos dois processos de replicação: carregar o conteúdo de pastas especificadas em um repositório local ou uma sincronização completa. Em uma sincronização completa, para cada uma das pastas especificadas, o conteúdo é carregado primeiro e, em seguida, baixado. Dependendo do conjunto *parâmetroulflags* na estrutura de **[sincronização](sync.md)** correspondente no estado de sincronização anterior, o Outlook inicializará [out] Membros na estrutura **SYNCCONT** para fornecer informações sobre o conteúdo. 
  
Através da mesma estrutura **SYNCCONT** , o cliente obtém a contagem das pastas que têm conteúdo a ser carregado ou baixado. O cliente executará um loop através de cada uma dessas pastas movendo o repositório local para o estado de carregamento da tabela para carregar uma pasta ou mover o repositório local para o estado de download da tabela para baixar a pasta. 
  
Além disso, o cliente obtém IDs de entrada para as pastas que requerem replicação.
  
Quando esse estado termina, o Outlook limpa suas informações internas. O repositório local retorna ao estado de sincronização.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

