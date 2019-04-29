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
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430928"
---
# <a name="deferring-processing"></a>Adiar o processamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Passe o sinalizador MAPI_DEFERRED_ERRORS para chamadas de método o máximo possível. Muitas das chamadas de método MAPI foram otimizadas para aceitar esse sinalizador, fazendo com que o provedor adie a tarefa solicitada até que várias tarefas possam ser executadas ao mesmo tempo ou você pode não esperar mais pelos resultados.
  
Por exemplo, se você passar MAPI_DEFERRED_ERRORS para [IMsgStore:: OpenEntry](imsgstore-openentry.md) para abrir uma pasta, a abertura da pasta e uma possível chamada remota poderão ser adiadas até que você faça outra chamada, como uma chamada para a GetHierarchyTable da pasta **** ou ** **Métodos GetProps. O **** GetHierarchyTable e o GetProps exigem o retorno de dados do provedor de serviços, uma tarefa que deve ser executada imediatamente. **** 
  
Outra maneira de adiar o processamento é simplesmente não fazer uma chamada. Ao ter conhecimento do usuário e quando o usuário pode perceber um dreno nos recursos ou tempo de processamento, você pode determinar quando faz sentido fazer chamadas. Há uma oportunidade de melhorar o desempenho fazendo chamadas em um momento em que o usuário não irá notar ou não fazendo isso.
  
Por exemplo, considere a situação em que você está recebendo mais de uma notificação por segundo de um repositório de mensagens que está movendo um grande número de mensagens. Um indicador de progresso é exibido para indicar a porcentagem da conclusão da operação. Normalmente, os usuários não perceberão que essa operação será lenta até que alguns segundos tenham passado. Portanto, se você estiver atualizando o indicador de progresso, não faça nenhuma alteração até pelo menos quatro segundos após o início da operação de movimentação. Isso poupará tempo nos casos comuns quando a operação for rápida e informará os usuários em tempo hábil quando a operação for lenta.
  

