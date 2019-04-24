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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334430"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Altera algumas ou todas as características de uma rotina ociosa baseada em [FNIDLE](fnidle.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
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

_FTG_
  
> no Marca de função que identifica a rotina ociosa. 
    
_pfnIdle_
  
> no Ponteiro para a rotina Idle. 
    
_pvIdleParam_
  
> no Ponteiro para um novo bloco de memória que a implementação de chamada aloca para a rotina ociosa. 
    
_priIdle_
  
> no O valor que representa uma nova prioridade para a rotina ociosa. As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores que zero, mas não zero. Um valor igual A zero é reservado para um evento de usuário, como um clique do mouse ou uma mensagem de WM_PAINT. Valores maiores do que zero representam prioridades para tarefas em segundo plano que têm uma prioridade maior do que os eventos de usuário e são despachados como parte do loop de bomba de mensagem do Windows padrão. Valores menores que zero representam prioridades para tarefas ociosas que só são executadas durante o tempo ocioso de bomba de mensagem. Os exemplos de prioridades são: 1 para envio de primeiro plano, 1 para a inserção de caracteres de edição de energia e 3 para baixar novas mensagens.
    
_csecIdle_
  
> no Um novo tempo, em centésimos de segundo, a ser aplicado à rotina ociosa. O significado do valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ . Pode ser: 
    
  - O período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez, se o sinalizador FIROWAIT estiver definido no _iroIdle_. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária. 
    
  - O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL estiver definido no _iroIdle_. 
    
_iroIdle_
  
> no Bitmask de sinalizadores que indicam novas opções para chamar a rotina de ociosidade. É necessário definir exatamente um dos seguintes sinalizadores:
    
  - FIROINTERVAL: o tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre chamadas sucessivas para a rotina ociosa. 
      
  - FIROONCEONLY: obsoleto. Não usar. 
      
  - FIROPERBLOCK: obsoleto. Não usar. 
      
  - FIROWAIT: o tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária. 
    
_ircIdle_
  
> no Bitmask dos sinalizadores usados para indicar que as alterações serão feitas na rotina ociosa. Os seguintes sinalizadores podem ser definidos em qualquer combinação:
    
  - FIRCCSEC: uma alteração no tempo associado à rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _csecIdle_ . 
      
  - FIRCIRO: uma alteração nas opções para a rotina de ociosidade, ou seja, uma alteração indicada pelo valor passado no parâmetro _iroIdle_ . 
      
  - FIRCPFN: uma alteração no ponteiro de rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _pfnIdle_ . 
      
  - FIRCPRI: uma alteração na prioridade da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _priIdle_ . 
      
  - FIRCPV: uma alteração no bloco de memória da rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _pvIdleParam_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do [FNIDLE](fnidle.md) : 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** aceitam como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  

