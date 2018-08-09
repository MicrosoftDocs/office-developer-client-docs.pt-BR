---
title: Sincronizar o estado do conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 216691f2c1f94d658a5aa968d6a19148a9b3c06a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770557"
---
# <a name="synchronize-contents-state"></a>Sincronizar o estado do conteúdo

  
  
**Aplica-se a**: Outlook 
  
 Este tópico descreve o que acontece durante o estado de conteúdo de sincronizar da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Estrutura de dados relacionados:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Desse estado:  <br/> |[Sincronizar o estado](synchronize-state.md) <br/> |
|Com esse estado:  <br/> |[Baixar o estado da tabela](download-table-state.md), [carregar o estado da tabela](upload-table-state.md), ou sincronizar o estado  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia um dos dois processos de replicação: carregar o conteúdo de especificado pastas em um repositório local ou uma sincronização completa. Em uma sincronização completa, para cada uma das pastas especificadas, o conteúdo é carregado pela primeira vez e então baixado. Dependendo da *ulFlags* definido na estrutura de **[sincronização](sync.md)** correspondente na anterior sincronizar o estado, Outlook inicializa [out] membros na estrutura de **SYNCCONT** para fornecer informações sobre o conteúdo. 
  
Através da mesma estrutura **SYNCCONT** , o cliente obtém a contagem das pastas que possuem conteúdo sejam carregados ou baixados. O cliente fará um loop através de cada uma dessas pastas movendo o armazenamento local para o estado da tabela de carregar para carregar uma pasta ou mover o repositório de local para o estado da tabela de download para baixar a pasta. 
  
Além disso, o cliente obtém IDs de entradas para as pastas que necessitam de replicação.
  
Quando for encerrada nesse estado, o Outlook limpa suas informações internas. Armazenamento local retorna ao estado sincronizar.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

