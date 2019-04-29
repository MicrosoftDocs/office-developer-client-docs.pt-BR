---
title: Carregar estado de status de leitura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431537"
---
# <a name="upload-read-status-state"></a>Carregar estado de status de leitura

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de upload de status de leitura da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPREAD](upread.md)** <br/> |
|A partir deste Estado:  <br/> |[Carregar estado da tabela](upload-table-state.md) <br/> |
|Para este Estado:  <br/> |Carregar estado da tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinista. Um cliente que faz parte de um estado para outro deve eventualmente retornar para o primeiro a partir do último. 
  
## <a name="description"></a>Descrição

Este estado inicia o carregamento do status de leitura dos itens em uma pasta especificada em um estado de tabela de carregamento anterior. Durante esse Estado, o Outlook Inicializa a estrutura de dados de **leitura** associada com informações para os itens na pasta cujo status de leitura foi alterado. O cliente atualiza o status de leitura desses itens no servidor como sendo lido ou não lido. 
  
Quando esse estado termina, o Outlook limpa as informações internas sobre o status de leitura do item, impedindo que o status de leitura do item seja carregado novamente. O repositório local retorna ao estado de carregamento da tabela.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

