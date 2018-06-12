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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0d3f24c41f2cfbd499d92e050c74da904dd4c377
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766631"
---
# <a name="ftgregisteridleroutine"></a>FtgRegisterIdleRoutine

**Aplica-se a**: Outlook 
  
Adiciona uma rotina ociosa [FNIDLE](fnidle.md) baseada em função para o sistema MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
FTG FtgRegisterIdleRoutine(
  PFNIDLE pfnIdle,
  LPVOID pvIdleParam,
  short priIdle,
  ULONG csecIdle,
  USHORT iroIdle
);
```

## <a name="parameters"></a>Par�metros

_pfnIdle_
  
> [in] Um ponteiro para a rotina ocioso. 
    
_pvIdleParam_
  
> [in] Um ponteiro para um bloco de memória que o mecanismo de ociosidade deve passar como um parâmetro para a rotina ociosa quando ele chama a ele. 
    
_priIdle_
  
> [in] A prioridade inicial para a rotina ociosa. Prioridades possíveis para rotinas definidos na implementação são maior ou menor do que zero, mas não a zero. A prioridade zero é reservada para um evento de usuário, como um clique do mouse ou de uma mensagem WM_PAINT. Prioridades maiores do que zero representam tarefas em segundo plano que têm uma prioridade maior que eventos do usuário e são enviadas como parte do loop de bomba de mensagem padrão do Windows. Prioridades menor do que zero representa ociosa tarefas a serem executadas somente durante o tempo ocioso de bomba de mensagem. Exemplos de prioridades são os seguintes: 1 para o envio de primeiro plano, 2 para inserção de energia-Editar caractere e 3 para baixar novas mensagens.
    
_csecIdle_
  
> [in] O valor de tempo inicial, em centésimos de segundos, a serem usados em especificar parâmetros de rotina ociosos. O significado de valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ . O significado pode ser um destes procedimentos: 
    
  - O período mínimo de ociosidade do usuário que deve transcorrer antes de MAPI mecanismo ocioso chama a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT for definido na _iroIdle_. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário. 
    
  - O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido na _iroIdle_. 
    
_iroIdle_
  
> [in] A bitmask dos sinalizadores usados para definir as opções iniciais para a rotina ociosa. Sinalizadores a seguir podem ser definidos:
    
  FIRONOADJUSTMENT
    
  > Use esse sinalizador para especificar que o timer de ociosidade de rotina não deve ser ajustado para suspensão ou continuar. O comportamento padrão sem esse sinalizador é que o tempo de espera é excluído ao calcular o tempo decorrido. Se FIRONOADJUSTMENT é passado, em seguida, o tempo de inatividade é incluído, ao calcular o tempo decorrido.
      
  FIRODISABLED
    
  > A rotina de ociosidade deve ser desabilitada quando registrado. A ação padrão é permitir a rotina ociosa quando **FtgRegisterIdleRoutine** registra a ele. 
      
  FIROINTERVAL 
    
  > O tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre sucessivas chamadas para a rotina ociosa. 
      
  FIROONCEONLY 
    
  > Obsoleto. Não a use. 
      
  FIROPERBLOCK 
    
  > Obsoleto. Não a use. 
      
  FIROWAIT 
    
  > O tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de ociosidade do usuário que deve transcorrer antes que a rotina ociosa chamada pelo mecanismo de ociosidade de MAPI pela primeira vez. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário. 
    
## <a name="return-value"></a>Valor retornado

A função de **FtgRegisterIdleRoutine** retornará uma marca de função que identifica a rotina ociosa que foi adicionada ao sistema de MAPI. Se **FtgRegisterIdleRoutine** não é possível registrar a rotina ociosa para o aplicativo cliente ou o provedor de serviço, por exemplo devido a problemas de memória, ele retornará NULL. 
  
## <a name="remarks"></a>Coment�rios

As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) . 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.  <br/> |
|**FtgRegisterIdleRoutine** <br/> |Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar. Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade. 
  
O exemplo a seguir é um exemplo de como usar o sinalizador FIRONOADJUSTMENT no parâmetro _iroIdle_ . 
  
1. Registre uma rotina de ociosidade com um atraso de 5 minutos.
    
2. Hibernação/suspensão o computador após 1 minuto (4 minutos deixado no cronômetro).
    
3. Reinicie o computador 10 minutos mais tarde.
    
O comportamento padrão, sem FIRONOADJUSTMENT, é que você ainda terá que aguardar 4 minutos mais para sua rotina executar. Ou seja, seu timer foi ajustada para permitir quanto tempo o computador estava suspenso. No entanto, se você passar FIRONOADJUSTMENT sua rotina ociosa será executado imediatamente porque decorridos mais de 5 minutos de tempo real.
  

