---
title: ChangeIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ChangeIdleRoutine
api_type:
- HeaderDef
ms.assetid: 0a24fe3b-a1ef-4748-b3b3-3bf747473c9d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cfec9356a866c79b687497c3af007c046a20a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418264"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Altera algumas ou todas as características de uma rotina ociosa baseada em [FNIDLE.](fnidle.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
VOID ChangeIdleRoutine(
  FTG ftg,
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle,
  USHORT ircIdle
);
```

## <a name="parameters"></a>Parâmetros

_ftg_
  
> [in] Marca de função que identifica a rotina ociosa. 
    
_pfnIdle_
  
> [in] Ponteiro para a rotina ociosa. 
    
_pvIdleParam_
  
> [in] Ponteiro para um novo bloco de memória que a implementação de chamada aloca para a rotina ociosa. 
    
_priIdle_
  
> [in] Valor que representa uma nova prioridade para a rotina ociosa. As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores do que zero, mas não zero. Um valor zero é reservado para um evento de usuário, como um clique do mouse ou uma WM_PAINT mensagem. Valores maiores do que zero representam prioridades para tarefas em segundo plano que têm uma prioridade mais alta do que os eventos do usuário e são enviados como parte do loop padrão de mensagem do Windows. Valores menores que zero representam prioridades para tarefas ociosas que só são executadas durante o tempo ocioso de mensagens. Exemplos de prioridades são: 1 para envio em primeiro plano, 1 para inserção de caracteres de edição de energia e 3 para baixar novas mensagens.
    
_csecIdle_
  
> [in] Um novo tempo, em centésimos de um segundo, a ser aplicado à rotina ociosa. O significado do valor de hora inicial varia, dependendo do que é passado no _parâmetro iroIdle._ Pode ser: 
    
  - O período mínimo de inação do usuário que deve passar antes que o mecanismo ocioso mapi chamar a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT estiver definido em  _iroIdle_. Depois que esse tempo passar, o mecanismo ocioso poderá chamar a rotina ociosa com a frequência necessária. 
    
  - O intervalo mínimo entre chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido em  _iroIdle_. 
    
_iroIdle_
  
> [in] Bitmask de sinalizadores indicando novas opções para chamar a rotina ociosa. Exatamente um dos seguintes sinalizadores deve ser definido:
    
  - FIROINTERVAL: o tempo especificado pelo parâmetro  _csecIdle_ é o intervalo mínimo entre chamadas sucessivas para a rotina ociosa. 
      
  - FIROONCEONLY: Obsoleto. Não usar. 
      
  - FIROPERBLOCK: obsoleto. Não usar. 
      
  - FIROWAIT: o tempo especificado pelo parâmetro  _csecIdle_ é o período mínimo de inação do usuário que deve passar antes que o mecanismo ocioso mapi chamar a rotina ociosa pela primeira vez. Depois que esse tempo passar, o mecanismo ocioso poderá chamar a rotina ociosa com a frequência necessária. 
    
_ircIdle_
  
> [in] Bitmask de sinalizadores usados para indicar as alterações a serem feitas na rotina ociosa. Os sinalizadores a seguir podem ser definidos em qualquer combinação:
    
  - FIRCCSEC: Uma alteração no tempo associado à rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _csecIdle._ 
      
  - FIRCIRO: Uma alteração nas opções para a rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _iroIdle._ 
      
  - FIRCPFN: Uma alteração no ponteiro de rotina ociosa, ou seja, uma alteração indicada pelo valor passado no _parâmetro pfnIdle._ 
      
  - FIRCPRI: Uma alteração na prioridade da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no _parâmetro priIdle._ 
      
  - FIRCPV: Uma alteração no bloco de memória da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _pvIdleParam._ 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md) 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Altera as características de uma rotina ociosa registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina ociosa registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  

