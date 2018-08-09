---
title: Interagir com um spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5cc1d0a8-ad23-4173-b220-b7c0169073fa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: faf3d48b63d1858a2b91f66c83d9ce08e9daa02b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767561"
---
# <a name="interacting-with-the-mapi-spooler"></a>Interagir com um spooler MAPI

  
  
**Aplica-se a**: Outlook 
  
Os métodos de [IXPLogon: IUnknown](ixplogoniunknown.md) interface são usados pelo spooler MAPI ao chamar o provedor de transporte. Ele deve ser possível para a maioria dos tipos de provedores de transporte para implementar a maioria desses métodos para que eles retornem rapidamente. Isso é desejável porque se um método leva muito tempo para retornar, em seguida, ele deve ser desmembrado com chamadas de volta para o spooler MAPI para liberar a CPU para outras tarefas. 
  
O MAPI spooler faz o seu trabalho e faz suas chamadas para provedores de transporte quando os aplicativos de primeiro plano ociosos. Depois de se desejar exibir caixas de diálogo quando o provedor de transporte primeiro tiver feito logon (governado pelas sinalizadores passados do MAPI para o provedor de transporte), provedores de transporte operam em segundo plano, a menos que chamado pelo cliente para liberar a enviar e receber filas. Filas de liberar é a única vez que um provedor de transporte não precisa release CPU e somente se o usuário é informado de que uma ação potencialmente longa está em andamento. O MAPI spooler geralmente solicita que um provedor de transporte liberar seus filas em resposta a uma ação do usuário, o provedor de transporte normalmente precisa fazer nada para garantir que o usuário é informado.
  
Um provedor de transporte pode decidir independentemente liberar uma fila e usar os bits STATUS_INBOUND_FLUSH e STATUS_OUTBOUND_FLUSH na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da sua linha de status para informar o spooler de MAPI que ele deseja atenção para que ele possa obter o trabalho feito. A linha de status é atualizada, usando o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Nesse caso, o provedor de transporte provavelmente deve exibir um indicador de progresso ou outra interface para informar ao usuário que está ocorrendo uma ação longa. 
  
Desde que a atividade de rede frequentemente leva a mais de 0,2 segundos, provedores de transporte devem, sempre que possível, use as solicitações de rede assíncrona. Isso permite que eles iniciar uma solicitação, liberar a CPU chamando volta para o spooler MAPI e quando o MAPI spooler novamente lhes controle, verifique se a sua solicitação de rede foi concluída. Se ele ainda não tiver sido concluído, eles release novamente a CPU chamando volta para o spooler MAPI com o método [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) . 
  
Durante a mensagem de processamento, entre [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) e [IXPLogon::EndMessage](ixplogon-endmessage.md) e durante a [IXPLogon::StartMessage](ixplogon-startmessage.md), o provedor de transporte normalmente faz muitas chamadas nos objetos expostos a ela pelo spooler MAPI. Como parte do seu tratamento desses objetos, o MAPI spooler ajuda ao provedor de transporte se comportam como um processo de plano de fundo apropriadamente, resultando em seu próprio quando apropriado. Um provedor de transporte que exigem o processamento de tempo crítico pode declarar uma seção crítica para o spooler MAPI usando o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) do objeto de suporte. Nesse caso, a CPU for lançada somente em chamadas de **SpoolerYield** explícitas pelo provedor de transporte até que o provedor de transporte termina com outra chamada para **SpoolerNotify**de processamento de seção crítica.
  
> [!NOTE]
> Isso não é o mesmo que uma seção crítica de Win32. Isso só deve ser feito quando o provedor de transporte precisa de um controle em tempo real dos recursos externos como ler dados de entrada de uma linha de fax. Como isso aumenta a prioridade do processo de spooler MAPI e pode causar a estação de trabalho não estar respondendo para a duração da operação, é uma boa ideia para notificar o usuário que uma ação potencialmente longa está em andamento e fornecer um indicador de progresso se possível. 
  

