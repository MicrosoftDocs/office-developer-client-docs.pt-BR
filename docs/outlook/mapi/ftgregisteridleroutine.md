---
title: FtgRegisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtgRegisterIdleRoutine
api_type:
- COM
ms.assetid: 8d9557ba-7919-42c6-9e2f-f10214437d53
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b45b80f09efbd4f05aabc2c868d5bd8eb5fa4cce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418518"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona uma rotina ociosa baseada em função [FNIDLE](fnidle.md) ao sistema MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Parâmetros

_pfnIdle_
  
> [in] Um ponteiro para a rotina ociosa. 
    
_pvIdleParam_
  
> [in] Um ponteiro para um bloco de memória que o mecanismo ocioso deve passar como um parâmetro para a rotina ociosa quando o chama. 
    
_priIdle_
  
> [in] A prioridade inicial para a rotina ociosa. As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores do que zero, mas não zero. A prioridade zero é reservada para um evento de usuário, como um clique do mouse ou uma WM_PAINT mensagem. Prioridades maiores do que zero representam tarefas em segundo plano que têm uma prioridade mais alta do que os eventos do usuário e são enviadas como parte do loop padrão de mensagens do Windows. Prioridades menores que zero representam tarefas ociosas que só são executadas durante o tempo ocioso da mensagem. Exemplos de prioridades são: 1 para envio em primeiro plano, 2 para inserção de caracteres de edição de energia e 3 para baixar novas mensagens.
    
_csecIdle_
  
> [in] O valor de tempo inicial, em centésimos de um segundo, a ser usado na especificação de parâmetros de rotina ocioso. O significado do valor de hora inicial varia, dependendo do que é passado no _parâmetro iroIdle._ O significado pode ser um dos seguintes: 
    
  - O período mínimo de inação do usuário que deve passar antes que o mecanismo ocioso mapi chamar a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT estiver definido em  _iroIdle_. Depois que esse tempo passar, o mecanismo ocioso poderá chamar a rotina ociosa com a frequência necessária. 
    
  - O intervalo mínimo entre chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido em  _iroIdle_. 
    
_iroIdle_
  
> [in] A bitmask de sinalizadores usada para definir opções iniciais para a rotina ociosa. Os sinalizadores a seguir podem ser definidos:
    
  FIRONOADJUSTMENT
    
  > Use esse sinalizador para especificar que o temporizador de rotina ociosa não deve ser ajustado para sleep ou resume. O comportamento padrão sem esse sinalizador é que o tempo de sleep é excluído ao calcular o tempo decorrido. Se FIRONOADJUSTMENT for passado, o tempo de sleep será incluído no cálculo do tempo decorrido.
      
  FIRODISABLED
    
  > A rotina ociosa deve ser desabilitada quando registrada. A ação padrão é habilitar a rotina ociosa **quando FtgRegisterIdleRoutine** a registra. 
      
  FIROINTERVAL 
    
  > O tempo especificado pelo parâmetro  _csecIdle_ é o intervalo mínimo entre chamadas sucessivas à rotina ociosa. 
      
  FIROONCEONLY 
    
  > Obsoleto. Não usar. 
      
  FIROPERBLOCK 
    
  > Obsoleto. Não usar. 
      
  FIROWAIT 
    
  > O tempo especificado pelo parâmetro  _csecIdle_ é o período mínimo de inação do usuário que deve passar antes que o mecanismo ocioso de MAPI chama a rotina ociosa pela primeira vez. Depois que esse tempo passar, o mecanismo ocioso poderá chamar a rotina ociosa com a frequência necessária. 
    
## <a name="return-value"></a>Valor de retorno

A **função FtgRegisterIdleRoutine** retorna uma marca de função que identifica a rotina ociosa que foi adicionada ao sistema MAPI. Se **FtgRegisterIdleRoutine** não puder registrar a rotina ociosa para o aplicativo cliente ou provedor de serviços, por exemplo, devido a problemas de memória, ele retornará NULL. 
  
## <a name="remarks"></a>Comentários

As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE.](fnidle.md) 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina ociosa registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina ociosa registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas em primeiro plano para a plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  
A seguir está um exemplo de como usar o sinalizador FIRONOADJUSTMENT no _parâmetro iroIdle._ 
  
1. Registre uma rotina ociosa com um atraso de 5 minutos.
    
2. Hibernar/insinuar o computador após 1 minuto (4 minutos no temporizador).
    
3. Retome o computador 10 minutos depois.
    
O comportamento padrão, sem FIRONOADJUSTMENT, é que você ainda precisa esperar mais 4 minutos para que sua rotina seja executado. Ou seja, seu temporizador foi ajustado para permitir por quanto tempo o computador ficou preso. No entanto, se você passar FIRONOADJUSTMENT, sua rotina ociosa será executado imediatamente porque mais de 5 minutos de tempo real decorram.
  

