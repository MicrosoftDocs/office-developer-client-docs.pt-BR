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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327990"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona uma rotina de ociosidade baseada na função [FNIDLE](fnidle.md) ao sistema MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
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
  
> no Um ponteiro para a rotina de ociosidade. 
    
_pvIdleParam_
  
> no Um ponteiro para um bloco de memória que o mecanismo de ociosidade deve passar como um parâmetro para a rotina ociosa quando ele chama. 
    
_priIdle_
  
> no A prioridade inicial para a rotina ociosa. As prioridades possíveis para rotinas definidas pela implementação são maiores ou menores que zero, mas não zero. A prioridade zero é reservada para um evento de usuário, como um clique do mouse ou uma mensagem WM_PAINT. As prioridades maiores do que zero representam tarefas em segundo plano que têm uma prioridade maior do que os eventos do usuário e são despachadas como parte do loop de bomba de mensagem padrão do Windows. Prioridades com menos de zero representam tarefas ociosas que só são executadas durante o tempo ocioso do bombeamento de mensagens. Exemplos de prioridades são: 1 para envio de primeiro plano, 2 para inserção de caracteres de edição de energia e 3 para baixar novas mensagens.
    
_csecIdle_
  
> no O valor inicial de tempo, em centésimos de segundo, a ser usado na especificação de parâmetros de rotina ociosa. O significado do valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ . O significado pode ser um dos seguintes: 
    
  - O período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez, se o sinalizador FIROWAIT estiver definido no _iroIdle_. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária. 
    
  - O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL estiver definido no _iroIdle_. 
    
_iroIdle_
  
> no A bitmask dos sinalizadores usados para definir as opções iniciais da rotina ociosa. Os seguintes sinalizadores podem ser definidos:
    
  FIRONOADJUSTMENT
    
  > Use este sinalizador para especificar que o timer de rotina ociosa não deve ser ajustado para Sleep ou resume. O comportamento padrão sem esse sinalizador é que o tempo de suspensão é excluído ao calcular o tempo decorrido. Se FIRONOADJUSTMENT for passado, o tempo de espera será incluído no cálculo do tempo decorrido.
      
  FIRODISABLED
    
  > A rotina ociosa deve ser desabilitada quando for registrada. A ação padrão é habilitar a rotina de ociosidade quando o **FtgRegisterIdleRoutine** o registra. 
      
  FIROINTERVAL 
    
  > O tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre chamadas sucessivas para a rotina ociosa. 
      
  FIROONCEONLY 
    
  > Obsoleto. Não usar. 
      
  FIROPERBLOCK 
    
  > Obsoleto. Não usar. 
      
  FIROWAIT 
    
  > O tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de inatividade do usuário que deve decorrer antes de o mecanismo de ociosidade de MAPI chamar a rotina de ociosidade pela primeira vez. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina de ociosidade com a frequência necessária. 
    
## <a name="return-value"></a>Valor de retorno

A função **FtgRegisterIdleRoutine** retorna uma marca de função identificando a rotina de ociosidade que foi adicionada ao sistema MAPI. Se o **FtgRegisterIdleRoutine** não puder registrar a rotina de ociosidade para o aplicativo cliente ou provedor de serviços, por exemplo, por causa de problemas de memória, ele retornará NULL. 
  
## <a name="remarks"></a>Comentários

As funções a seguir lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função [FNIDLE](fnidle.md) . 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** aceitam como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  
Veja a seguir um exemplo de como usar o sinalizador FIRONOADJUSTMENT no parâmetro _iroIdle_ . 
  
1. Registrar uma rotina ociosa com atraso de 5 minutos.
    
2. Hibernar/dormir o computador após 1 minuto (4 minutos restantes no temporizador).
    
3. ReTome o computador 10 minutos mais tarde.
    
O comportamento padrão, sem o FIRONOADJUSTMENT, é que você ainda precisa aguardar mais 4 minutos para que a rotina seja executada. Ou seja, o cronômetro foi ajustado para permitir por quanto tempo o computador estava em suspensão. No enTanto, se você passar FIRONOADJUSTMENT sua rotina de ociosidade será executada imediatamente porque decorrido mais de cinco minutos de tempo real.
  

