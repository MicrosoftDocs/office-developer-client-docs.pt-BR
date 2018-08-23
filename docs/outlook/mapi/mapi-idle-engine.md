---
title: Mecanismo de ociosidade de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9fdc254053c2d35c83866bd8a076279fd383db02
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583033"
---
# <a name="mapi-idle-engine"></a>Mecanismo de ociosidade de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI fornece várias funções que são conhecidas coletivamente como o mecanismo de ocioso. Essas funções permitem que os clientes, provedores de catálogo de endereços e provedores de armazenamento de mensagem realizar várias tarefas nos momentos lentos na sessão ou em resposta a um longo período. Por exemplo, clientes e provedores de serviços podem adiar operações lentas ou fechar arquivos que permaneceram não utilizados por um longo período. Provedores de transporte normalmente não usam o mecanismo de ociosidade porque o método **IXPLogon::Idle** assume seu lugar. Para obter mais informações, consulte [IXPLogon::Idle](ixplogon-idle.md).
  
Para usar o mecanismo de ociosidade, clientes e provedores de serviço criam uma função de retorno de chamada que contém as tarefas que devem ocorrer quando o subsistema de MAPI estiver ocioso. Quando o MAPI detecta tempo ocioso, ele chama essa função de retorno de chamada. A função de retorno de chamada segue protótipo **FNIDLE** , definido da seguinte forma: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Para obter mais informações, consulte [FNIDLE](fnidle.md).
  
As funções que compõem o mecanismo de ociosidade são:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Para registrar uma função de retorno de chamada, clientes e provedores de serviços chamam a função de **FtgRegisterIdleRoutine** . Os parâmetros de entrada incluem uma prioridade opcional, um bloco de memória que é passado para sua função de retorno de chamada como entrada, uma quantidade de tempo para ser usado de forma alguma apropriada, e os sinalizadores de um conjunto de opção. 
  
Clientes e provedores de serviços podem especifique uma prioridade no parâmetro _priIdle_ que controla como a função ociosa é executado ou zero se prioridade não for um problema. Como os números negativos representam as prioridades mais altas que números positivos ou zero, operações de compactação e de pesquisa devem ser atribuídas a números negativos. Tarefas que ocorrem uma vez devem ser atribuídas a números positivos. 
  
Para cancelar o registro de uma função de retorno de chamada ativa, clientes e provedores de serviços chamam a função de **DeregisterIdleRoutine** . Como **DeregisterIdleRoutine** opera de forma assíncrona, é possível para a função de retorno de chamada a ser chamado a qualquer momento durante a chamada de cancelar registro e, possivelmente, até mesmo após **DeregisterIdleRoutine** ter retornado. 
  
Para modificar algumas ou todas as características de uma função de retorno de chamada, clientes e provedores de serviços chamam a função de **ChangeIdleRoutine** . **ChangeIdleRoutine** torna muda de acordo com como o parâmetro de sinalizadores _ircIdle_ estiver definida; **ChangeIdleRoutine** pode alterar a própria função, sua prioridade, configuração de tempo e o parâmetro de entrada. 
  
MAPI define ocioso o mesmo que o sistema operacional, quando o sistema operacional tem uma definição. No Win32, MAPI cria um segmento com prioridade de classe de ociosidade para agendar tarefas ociosas. Esse thread controla o tempo e posta uma mensagem para o segmento que deverá executar a tarefa ociosa quando chegar a hora para sua execução. Win32 agenda threads, não processa. Se as tarefas que têm uma prioridade maior do que a prioridade ociosa estão ocorrendo na estação de trabalho, a tarefa ociosa não deve agendada para execução até concluir as tarefas. 
  
Todas as tarefas ociosas são executados no segmento que chamado **MAPIInitIdle**. MAPI tem um segmento separado para agendamento, mas quando uma tarefa ociosa fica elegível, ele posta uma mensagem novamente sobre para o thread de inicialização e a tarefa ociosa é executada lá. As implicações para diferentes tipos de clientes são os seguintes.
  
|**Modelo de Threading**|**Implicação**|
|:-----|:-----|
|Com um único segmento  <br/> |Não há problema. Funções ociosas executar no thread principal do seu cliente e são serializadas através do loop de mensagem.  <br/> |
|Encadeamento livre  <br/> |Funções ociosas devem ser thread-safe, mas seu cliente já tiver a infra-estrutura necessária. Seu cliente não talvez seja necessário em todos os o mecanismo de ociosidade de MAPI.  <br/> |
|Apartamento  <br/> |Função ociosa tem de ser executados no mesmo thread que o registrou se deseja usar MAPI, OLE ou qualquer outros interfaces COM. A maneira mais simples é registrar uma função ociosa com MAPI que posta uma mensagem para a direita thread e expedir a função "real" ociosa diretamente do loop de mensagem desse segmento.  <br/> |
   

