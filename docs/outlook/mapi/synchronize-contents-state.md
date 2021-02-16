---
title: Sincronizar o estado do conteúdo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 52216bc3-8cbd-3856-ea46-78f7d0dd66ff
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ebe1f5f48f9becdf01ea184c2b76fa2c8fa21e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438467"
---
# <a name="synchronize-contents-state"></a>Sincronizar o estado do conteúdo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de sincronização do conteúdo da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_CONTENTS** <br/> |
|Estrutura de dados relacionada:  <br/> |**[SYNCCONT](synccont.md)** <br/> |
|Desse estado:  <br/> |[Estado Sincronizar](synchronize-state.md) <br/> |
|Para esse estado:  <br/> |[Estado de download da tabela,](download-table-state.md) [estado de carregamento da](upload-table-state.md)tabela ou estado de sincronização  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia um dos dois processos de replicação: carregar o conteúdo das pastas especificadas em um armazenamento local ou uma sincronização completa. Em uma sincronização completa, para cada uma das pastas especificadas, o conteúdo é carregado primeiro e, em seguida, baixado. Dependendo do  *ulFlags*  definido na estrutura **[SYNC](sync.md)** correspondente no estado de sincronização anterior, o Outlook inicializa membros [out] na estrutura **SYNCCONT** para fornecer informações sobre o conteúdo. 
  
Por meio da mesma **estrutura SYNCCONT,** o cliente obtém a contagem das pastas que têm conteúdo a ser carregado ou baixado. O cliente fará um loop por cada uma dessas pastas movendo o armazenamento local para o estado carregar tabela para carregar uma pasta ou movendo o armazenamento local para o estado de tabela de download para baixar a pasta. 
  
Além disso, o cliente obtém IDs de entrada para as pastas que exigem replicação.
  
Quando esse estado termina, o Outlook limpa suas informações internas. O armazenamento local retorna ao estado de sincronização.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

