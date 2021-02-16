---
title: Interagindo com o Spooler MAPI
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
# <a name="interacting-with-the-mapi-spooler"></a>Interagindo com o Spooler MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os métodos na interface [IXPLogon : IUnknown](ixplogoniunknown.md) são usados pelo spooler MAPI ao chamar o provedor de transporte. Deve ser possível que a maioria dos tipos de provedores de transporte implemente a maioria desses métodos para que eles retornem rapidamente. Isso é desejável porque, se um método levar muito tempo para retornar, ele deverá ser dividido com chamadas de volta para o spooler MAPI para liberar a CPU para outras tarefas. 
  
O spooler MAPI faz seu trabalho e faz suas chamadas para provedores de transporte quando os aplicativos em primeiro plano estão ociosos. Depois de exibir opcionalmente caixas de diálogo quando o provedor de transporte é conectado pela primeira vez (regido por sinalizadores passados de MAPI para o provedor de transporte), os provedores de transporte operam em segundo plano, a menos que seja chamado pelo cliente para liberar filas de envio e recebimento. Liberar filas é a única vez que um provedor de transporte não precisa liberar a CPU e, em seguida, somente se o usuário for informado de que uma ação potencialmente longa está em andamento. O spooler MAPI normalmente solicita que um provedor de transporte libera suas filas em resposta a uma ação do usuário, portanto, o provedor de transporte normalmente não precisa fazer nada para garantir que o usuário seja informado.
  
Um provedor de transporte pode decidir independentemente liberar uma fila e usar os bits STATUS_INBOUND_FLUSH e STATUS_OUTBOUND_FLUSH na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sua linha de status para informar ao spooler MAPI que ele deseja atenção para que ele possa fazer o trabalho. A linha de status é atualizada usando o [método IMAPISupport::ModifyStatusRow.](imapisupport-modifystatusrow.md) Nesse caso, o provedor de transporte provavelmente deve exibir um indicador de progresso ou outra interface para informar ao usuário que uma ação longa está ocorrendo. 
  
Como a atividade de rede geralmente leva mais de 0,2 segundos, os provedores de transporte devem, sempre que possível, usar solicitações de rede assíncronas. Isso permite que eles iniciem uma solicitação, liberem a CPU chamando de volta para o spooler MAPI e, quando o spooler MAPI novamente lhes dá controle, para verificar se sua solicitação de rede foi concluída. Se ele ainda não tiver sido concluído, eles liberarão novamente a CPU chamando de volta para o spooler MAPI com o método [IMAPISupport::SpoolerYield.](imapisupport-spooleryield.md) 
  
Durante o processamento de mensagens, entre [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) e [IXPLogon::EndMessage](ixplogon-endmessage.md) e durante [IXPLogon::StartMessage](ixplogon-startmessage.md), o provedor de transporte normalmente faz muitas chamadas em objetos expostos a ele pelo spooler MAPI. Como parte de sua manipulação desses objetos, o spooler MAPI ajuda o provedor de transporte a se comportar adequadamente como um processo em segundo plano, segurando sozinho quando apropriado. Um provedor de transporte que exige processamento crítico de tempo pode declarar uma seção crítica para o spooler MAPI usando o método de objeto de suporte [IMAPISupport::SpoolerNotify.](imapisupport-spoolernotify.md) Nesse caso, a CPU é liberada somente em chamadas **SpoolerYield** explícitas pelo provedor de transporte até que o provedor de transporte termine o processamento de seção crítica com outra chamada para **SpoolerNotify**.
  
> [!NOTE]
> Isso não é o mesmo que uma seção crítica do Win32. Isso só deve ser feito quando o provedor de transporte precisar de controle em tempo real de recursos externos, como a leitura de dados de entrada de uma linha de fax. Como isso aumenta a prioridade do processo de spooler MAPI e pode fazer com que a estação de trabalho não seja responsiva pela duração da operação, é uma boa ideia notificar o usuário de que uma ação potencialmente longa está em andamento e fornecer um indicador de progresso, se possível. 
  

