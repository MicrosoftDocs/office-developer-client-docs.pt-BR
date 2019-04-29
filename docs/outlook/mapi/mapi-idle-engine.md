---
title: Mecanismo ocioso de MAPI
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
# <a name="mapi-idle-engine"></a>Mecanismo ocioso de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI fornece várias funções que são conhecidas coletivamente como o mecanismo de ociosidade. Essas funções permitem que clientes, provedores de catálogos de endereços e provedores de repositório de mensagens executem várias tarefas durante tempos lentos na sessão ou em resposta a um tempo lento. Por exemplo, clientes e provedores de serviço podem adiar operações lentas ou fechar arquivos que permaneceram não utilizados por um período longo. Geralmente, os provedores de transporte não usam o mecanismo de ociosidade, pois o método **IXPLogon:: Idle** usa seu lugar. Para obter mais informações, consulte [IXPLogon:: Idle](ixplogon-idle.md).
  
Para usar o mecanismo de ociosidade, os clientes e provedores de serviço criam uma função de retorno de chamada que contém as tarefas que devem ocorrer quando o subsistema MAPI estiver ocioso. Quando o MAPI detecta o tempo ocioso, ele invoca essa função de retorno de chamada. A função de retorno de chamada segue o protótipo **FNIDLE** , definido da seguinte maneira: 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
Para obter mais informações, consulte [FNIDLE](fnidle.md).
  
As funções que compõem o mecanismo de ociosidade são:
  
[ChangeIdleRoutine](changeidleroutine.md)
  
[DeregisterIdleRoutine](deregisteridleroutine.md)
  
[EnableIdleRoutine](enableidleroutine.md)
  
[FtgRegisterIdleRoutine](ftgregisteridleroutine.md)
  
[MAPIDeInitIdle](mapideinitidle.md)
  
[MAPIInitIdle](mapiinitidle.md)
  
Para registrar uma função de retorno de chamada, os clientes e provedores de serviços chamam a função **FtgRegisterIdleRoutine** . Os parâmetros de entrada incluem uma prioridade opcional, um bloco de memória que é passado para a função de retorno de chamada como entrada, uma quantidade de tempo a ser usada de qualquer forma apropriada e um conjunto de sinalizadores de opção. 
  
Os clientes e provedores de serviços podem especificar uma prioridade no parâmetro _priIdle_ que controla como a função ociosa é executada ou especificar zero se a prioridade não for um problema. Como números negativos representam prioridades mais altas do que números positivos ou zero, as operações de compactação e de pesquisa devem ser atribuídas a números negativos. As tarefas que ocorrem uma vez devem ser atribuídas a números positivos. 
  
Para cancelar o registro de uma função de retorno de chamada ativa, os clientes e os provedores de serviços chamam a função **DeregisterIdleRoutine** . Como o **DeregisterIdleRoutine** funciona de forma assíncrona, é possível que a função de retorno de chamada seja invocada a qualquer momento durante a chamada de cancelamento de registro e, possivelmente, mesmo após o **DeregisterIdleRoutine** ter retornado. 
  
Para modificar algumas ou todas as características de uma função de retorno de chamada, os clientes e provedores de serviços chamam a função **ChangeIdleRoutine** . **ChangeIdleRoutine** faz alterações de acordo com o modo como o parâmetro flags _ircIdle_ é definido; **ChangeIdleRoutine** pode alterar a própria função, sua prioridade, configuração de tempo e parâmetro de entrada. 
  
O MAPI define o mesmo ociosidade do sistema operacional, quando o sistema operacional tem uma definição. No Win32, o MAPI cria um thread com prioridade de classe ociosa para agendar tarefas ociosas. Este thread mantém o controle do tempo e envia uma mensagem para o thread que deve executar a tarefa ociosa quando o tempo de sua execução chegar. O Win32 agenda threads, não processos. Se as tarefas que têm uma prioridade maior do que a prioridade de ociosidade estiverem ocorrendo na estação de trabalho, a tarefa ociosa não deve ser agendada para execução até que as tarefas tenham sido concluídas. 
  
Todas as tarefas ociosas são executadas no thread que chamou **MAPIInitIdle**. O MAPI tem um thread separado para agendamento, mas quando uma tarefa ociosa se torna qualificada, ela envia uma mensagem de volta para o thread de inicialização e a tarefa ociosa é executada lá. As implicações para diferentes tipos de clientes são as seguintes.
  
|**Modelo de segmentação**|**Implícito**|
|:-----|:-----|
|Thread único  <br/> |Não há problema. As funções ociosas são executadas no thread principal do cliente e são serializadas por meio do loop de mensagem.  <br/> |
|Livre-segmentado  <br/> |As funções ociosas devem ser thread-safe, mas o cliente já tem a infraestrutura necessária. O cliente pode não precisar do mecanismo de ociosidade de MAPI.  <br/> |
|Segmentação de apartamento  <br/> |A função Idle deve ser executada no mesmo thread que o registrou, se quiser usar MAPI, OLE ou qualquer outra interface COM. A maneira mais simples é registrar uma função ociosa com MAPI que envia uma mensagem para o thread certo e despachar a função ociosa "real" diretamente do loop de mensagens desse thread.  <br/> |
   

