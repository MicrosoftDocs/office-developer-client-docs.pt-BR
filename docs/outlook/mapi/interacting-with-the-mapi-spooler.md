---
title: Interagir com o spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: da94347dcb47e5fdbd4a6c1d404b795f4f7938ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432146"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interagir com o spooler MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os métodos na interface [IXPLogon: IUnknown](ixplogoniunknown.md) são usados pelo spooler MAPI ao chamar o provedor de transporte. Deve ser possível para a maioria dos tipos de provedores de transporte implementar a maioria desses métodos para que eles retornem rapidamente. Isso é desejável porque se um método levar muito tempo para retornar, deve ser dividido com chamadas de volta para o spooler MAPI para liberar a CPU para outras tarefas. 
  
O MAPI spooler funciona e faz suas chamadas para provedores de transporte quando os aplicativos de primeiro plano estiverem ociosos. Após exibir opcionalmente caixas de diálogo quando o provedor de transporte é conectado pela primeira vez (regido pelos sinalizadores passados de MAPI para o provedor de transporte), os provedores de transporte operam em segundo plano, a menos que o cliente tenha sido chamado pelo cliente para liberar as filas de envio e recebimento. A liberação de filas é a única vez que um provedor de transporte não precisa liberar a CPU e, em seguida, somente se o usuário for informado de que uma ação possivelmente longa está em andamento. O spooler MAPI normalmente solicita que um provedor de transporte libere suas filas em resposta a uma ação do usuário, portanto, o provedor de transporte normalmente não precisa fazer nada para garantir que o usuário seja informado.
  
Um provedor de transporte pode decidir de forma independente a liberação de uma fila e usar os bits STATUS_INBOUND_FLUSH e STATUS_OUTBOUND_FLUSH na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sua linha de status para informar ao spooler MAPI que ele deseja atenção para que possa realizar o trabalho. A linha de status é atualizada usando o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . Nesse caso, o provedor de transporte deve provavelmente exibir um indicador de progresso ou outra interface para informar ao usuário que uma ação longa está ocorrendo. 
  
Como a atividade de rede geralmente leva mais de 0,2 segundos, os provedores de transporte devem, sempre que possível, usar solicitações de rede assíncronas. Isso permite que eles iniciem uma solicitação, liberem a CPU ligando de volta ao spooler MAPI e, quando o spooler MAPI der novamente controle, verifique se a solicitação de rede foi concluída. Se ele ainda não tiver sido concluído, libere novamente a CPU ligando de volta ao spooler MAPI com o método [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) . 
  
Durante o processamento de mensagens, entre [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) e [IXPLogon:: endmessage](ixplogon-endmessage.md) e durante [IXPLogon:: StartMessage](ixplogon-startmessage.md), o provedor de transporte geralmente faz muitas chamadas em objetos expostos a ele pelo spooler MAPI. Como parte de sua manipulação desses objetos, o spooler MAPI ajuda o provedor de transporte a se comportar apropriadamente como um processo de plano de fundo por meio de seu próprio, quando apropriado. Um provedor de transporte que requer o processamento de tempo crítico pode declarar uma seção crítica para o spooler MAPI usando o método de objeto de suporte [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . Nesse caso, a CPU é liberada somente em chamadas **SpoolerYield** explícitas pelo provedor de transporte até que o provedor de transporte termine o processamento de seção crítico com outra chamada para **SpoolerNotify**.
  
> [!NOTE]
> Isso não é o mesmo que uma seção crítica do Win32. Isso deve ser feito apenas quando o provedor de transporte precisa de controle em tempo real de recursos externos, como a leitura de dados de entrada de uma linha de fax. Como isso gera a prioridade do processo de spooler MAPI e pode fazer com que a estação de trabalho pare de responder pela duração da operação, é uma boa ideia notificar o usuário de que uma ação possivelmente longa está em andamento e fornecer um indicador de progresso, se possível. 
  

