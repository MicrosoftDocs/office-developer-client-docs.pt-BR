---
title: Carregar Estado de Status de Leitura
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
# <a name="upload-read-status-state"></a>Carregar Estado de Status de Leitura

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Este tópico descreve o que acontece durante o estado de status de leitura do upload da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de Estado:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Estrutura de dados relacionada:  <br/> |**[UPREAD](upread.md)** <br/> |
|Desse estado:  <br/> |[Estado carregar tabela](upload-table-state.md) <br/> |
|Para esse estado:  <br/> |Estado carregar tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinística. Um cliente que sai de um estado para outro eventualmente deve retornar ao primeiro do último. 
  
## <a name="description"></a>Descrição

Esse estado inicia o upload do status de leitura dos itens em uma pasta especificada em um estado de tabela de carregamento anterior. Durante esse estado, o Outlook inicializa a estrutura de dados **UPREAD** associada com informações para esses itens na pasta cujo status de leitura foi alterado. Em seguida, o cliente atualiza o status de leitura desses itens no servidor como lidos ou não lidos. 
  
Quando esse estado termina, o Outlook limpa as informações internas sobre o status de leitura do item, impedindo que o status de leitura do item seja carregado novamente. O armazenamento local retorna ao estado da tabela de carregamento.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[SYNCSTATE](syncstate.md)

