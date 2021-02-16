---
title: Mecanismo ocioso MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d8d591c02bb621c16a1d1b46272b19573ea79785
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428449"
---
# <a name="mapi-idle-engine"></a>Mecanismo ocioso MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI fornece várias funções que são coletivamente conhecidas como mecanismo ocioso. Essas funções permitem que clientes, provedores de livros de endereços e provedores de armazenamento de mensagens realizem várias tarefas durante horários lentos na sessão ou em resposta a um tempo lento. Por exemplo, clientes e provedores de serviços podem adiar operações lentas ou fechar arquivos que permaneceram inutilizados por um longo período. Os provedores de transporte normalmente não usam o mecanismo ocioso porque o **método IXPLogon::Idle** assume seu lugar. Para obter mais informações, consulte [IXPLogon::Idle](ixplogon-idle.md).
  
Para usar o mecanismo ocioso, os clientes e provedores de serviços criam uma função de retorno de chamada que contém as tarefas que devem ocorrer quando o subsistema MAPI está ocioso. Quando o MAPI detecta o tempo ocioso, ele invoca essa função de retorno de chamada. A função de retorno de chamada segue o protótipo **FNIDLE,** definido da seguinte forma: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Para obter mais informações, consulte [FNIDLE](fnidle.md).
  
As funções que compom o mecanismo ocioso são:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Para registrar uma função de retorno de chamada, os clientes e provedores de serviços chamam a **função FtgRegisterIdleRoutine.** Os parâmetros de entrada incluem uma prioridade opcional, um bloco de memória que é passado para a função de retorno de chamada como entrada, um tempo a ser usado de qualquer maneira apropriado e um conjunto de sinalizadores de opção. 
  
Clientes e provedores de serviços podem especificar uma prioridade no parâmetro  _priIdle_ que controla como a função ociosa é executado ou especificar zero se a prioridade não for um problema. Como os números negativos representam prioridades maiores do que números positivos ou zero, as operações de compactação e pesquisa devem ser atribuídas a números negativos. Tarefas que ocorrem uma vez devem ser atribuídas números positivos. 
  
Para desregister uma função de retorno de chamada ativa, os clientes e provedores de serviços chamam a **função DeregisterIdleRoutine.** Como **DeregisterIdleRoutine** opera de forma assíncrona, é possível que a função de retorno de chamada seja invocada a qualquer momento durante a chamada do desregister e, possivelmente, mesmo depois que **DeregisterIdleRoutine** tiver retornado. 
  
Para modificar algumas ou todas as características de uma função de retorno de chamada, os clientes e provedores de serviços chamam a **função ChangeIdleRoutine.** **ChangeIdleRoutine** faz alterações de acordo com como o parâmetro  _de sinalizadores ircIdle_ é definido; **ChangeIdleRoutine pode** alterar a função propriamente dita, sua prioridade, configuração de hora e parâmetro de entrada. 
  
O MAPI define ocioso da mesma forma que o sistema operacional, quando o sistema operacional tem uma definição. No Win32, o MAPI cria um thread com prioridade de classe ociosa para agendar tarefas ociosas. Esse thread mantém o controle do tempo e posta uma mensagem no thread que deve executar a tarefa ociosa quando chegar a hora de sua execução. O Win32 agenda threads, não processos. Se tarefas com prioridade maior do que a prioridade de ociosidade ocorrerem na estação de trabalho, a tarefa ociosa não deverá ser agendada para execução até que as tarefas sejam concluídas. 
  
Todas as tarefas ociosas são executadas no thread que **chamou MAPIInitIdle**. MAPI has a separate thread for scheduling, but when an idle task becomes eligible, it posts a message back over to the initialization thread and the idle task is executed there. As implicações para diferentes tipos de clientes são as a seguir.
  
|**Modelo de threading**|**Implicação**|
|:-----|:-----|
|Single-threaded  <br/> |Não tem problema. As funções ociosas são executadas no thread principal do cliente e são serializadas por meio do loop da mensagem.  <br/> |
|Threaded livre  <br/> |As funções ociosas devem ser thread-safe, mas seu cliente já tem a infraestrutura necessária. Seu cliente pode não precisar do mecanismo ocioso MAPI.  <br/> |
|Apartment threaded  <br/> |A função Idle precisa ser executada no mesmo thread que a registrou se quiser usar MAPI, OLE ou outras interfaces COM. A maneira mais simples é registrar uma função ociosa com MAPI que posta uma mensagem no thread direito e despachar a função ociosa "real" diretamente do loop de mensagens desse thread.  <br/> |
   

