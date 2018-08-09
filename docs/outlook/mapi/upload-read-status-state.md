---
title: Carregar o estado do status de leitura
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 172eaf47d305cf6e4d1ba54ceb4ac4b4feab80e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770675"
---
# <a name="upload-read-status-state"></a>Carregar o estado do status de leitura

  
  
**Aplica-se a**: Outlook 
  
 Este tópico descreve o que acontece durante o carregamento ler o estado de status da máquina de estado de replicação. 
  
## <a name="quick-info"></a>Informações rápidas

|||
|:-----|:-----|
|Identificador de controle de sessão:  <br/> |**LR_SYNC_UPLOAD_MESSAGE_READ** <br/> |
|Estrutura de dados relacionados:  <br/> |**[UPREAD](upread.md)** <br/> |
|Desse estado:  <br/> |[Carregar o estado da tabela](upload-table-state.md) <br/> |
|Com esse estado:  <br/> |Carregar o estado da tabela  <br/> |
   
> [!NOTE]
> A máquina de estado de replicação é uma máquina de estado determinantes. Um cliente partindo de um estado para outro eventualmente deve retornar para o anterior do último. 
  
## <a name="description"></a>Descrição

Nesse estado inicia o carregamento do status de itens em uma pasta especificada em um estado de tabela anterior do carregamento leitura. Durante esse estado, o Outlook inicializa a estrutura de dados **UPREAD** associada com informações para os itens na pasta cujo status de leitura foi alterada. O cliente, em seguida, atualiza o status de leitura desses itens no servidor como sendo lidos ou não lidos. 
  
Quando for encerrada nesse estado, o Outlook limpa as informações internas sobre o status do item leitura, impedindo que o status de leitura do item que está sendo carregado novamente. Armazenamento local retorna para o estado da tabela de carregamento.
  
## <a name="see-also"></a>Confira também



[Sobre a API de replicação](about-the-replication-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[Sobre a máquina de estado de replicação](about-the-replication-state-machine.md)
  
[ESTADO DE SINCRONIZAÇÃO](syncstate.md)

