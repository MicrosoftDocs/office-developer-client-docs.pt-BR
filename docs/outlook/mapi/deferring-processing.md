---
title: Adiar o processamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c4577a35315c9df0055e97de26dd0baf1a2b489
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580583"
---
# <a name="deferring-processing"></a>Adiar o processamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Passe o sinalizador MAPI_DEFERRED_ERRORS às chamadas do método tanto quanto possível. Muitas das chamadas MAPI método foram otimizadas para aceitar esse sinalizador, fazendo com que o provedor ou adiar a tarefa solicitada até várias tarefas podem ser executadas simultaneamente ou você pode esperar que não são mais os resultados.
  
Por exemplo, se você passar MAPI_DEFERRED_ERRORS para [IMsgStore::OpenEntry](imsgstore-openentry.md) para abrir uma pasta, a abertura da pasta e uma chamada remota possível possa ser adiada até você fazer outra chamada como uma chamada para **GetHierarchyTable** da pasta ou o ** GetProps** métodos. **GetHierarchyTable** e o **GetProps** exigem o retorno de dados do provedor do serviço, uma tarefa que deve ser executado imediatamente. 
  
Outra maneira para adiar o processamento é simplesmente não para fazer uma chamada. Ao ser ciente do usuário e o usuário pode percebem diminui o tempo de processamento ou recursos, você pode determinar quando fizer sentido para fazer chamadas. Não há uma oportunidade para melhorar o desempenho fazendo chamadas a cada vez quando o usuário não notarão ou por não torná-los.
  
Por exemplo, considere a situação quando você está recebendo mais de uma notificação por segundo de um repositório de mensagem que está se movendo um grande número de mensagens. Um indicador de progresso é exibido para indicar a porcentagem de conclusão da operação. Os usuários geralmente não serão percebam esta operação para ser lenta enquanto alguns segundos passados. Portanto, se você estiver atualizando o indicador de progresso, não faça qualquer alteração até pelo menos quatro segundos após o início da operação de movimentação. Isso irá economizar tempo nos casos comuns quando a operação é fast e informar os usuários de modo oportuno quando a operação está lenta.
  

