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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1fbeccd805953322b579d1490b5e74e5132aa7ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766301"
---
# <a name="changeidleroutine"></a>ChangeIdleRoutine

**Aplica-se a**: Outlook 
  
Altera algumas ou todas as características de uma rotina de ociosidade [FNIDLE](fnidle.md) com base. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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

## <a name="parameters"></a>Par�metros

_ftg_
  
> [in] Marca de função que identifica a rotina ociosa. 
    
_pfnIdle_
  
> [in] Ponteiro para a rotina ocioso. 
    
_pvIdleParam_
  
> [in] Ponteiro para um novo bloco de memória que a implementação chamando aloca para a rotina ociosa. 
    
_priIdle_
  
> [in] Valor que representa uma nova prioridade para a rotina ociosa. Prioridades possíveis para rotinas definidos na implementação são maior ou menor do que zero, mas não a zero. Um valor de zero é reservado para um evento de usuário, como um clique do mouse ou de uma mensagem WM_PAINT. Valores maiores que zero representam as prioridades de tarefas em segundo plano que têm uma prioridade maior que eventos do usuário e são enviadas como parte do loop de bomba de mensagem padrão do Windows. Valores inferiores a zero representam as prioridades de ociosidade tarefas a serem executadas somente durante o tempo ocioso da mensagem de retângulos. Exemplos de prioridades são: 1 para o envio de primeiro plano, 1 para inserção de energia-Editar caractere e 3 para baixar novas mensagens.
    
_csecIdle_
  
> [in] Um novo tempo, em centésimos de segundos, para aplicar a rotina ociosa. O significado de valor de tempo inicial varia, dependendo do que é passado no parâmetro _iroIdle_ . Ele pode ser: 
    
  - O período mínimo de ociosidade do usuário que deve transcorrer antes de MAPI mecanismo ocioso chama a rotina ociosa pela primeira vez, se o sinalizador FIROWAIT for definido na _iroIdle_. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário. 
    
  - O intervalo mínimo entre as chamadas para a rotina ociosa, se o sinalizador FIROINTERVAL for definido na _iroIdle_. 
    
_iroIdle_
  
> [in] Bitmask dos sinalizadores indicando novas opções para chamar a rotina ociosa. Exatamente um dos sinalizadores a seguir deve ser definido:
    
  - FIROINTERVAL: O tempo especificado pelo parâmetro _csecIdle_ é o intervalo mínimo entre sucessivas chamadas para a rotina ociosa. 
      
  - FIROONCEONLY: obsoleto. Não a use. 
      
  - FIROPERBLOCK: obsoleto. Não a use. 
      
  - FIROWAIT: O tempo especificado pelo parâmetro _csecIdle_ é o período mínimo de ociosidade do usuário que deve transcorrer antes que a rotina ociosa chamada pelo mecanismo de ociosidade de MAPI pela primeira vez. Após esse tempo, o mecanismo de ociosidade pode chamar a rotina ociosa sempre que for necessário. 
    
_ircIdle_
  
> [in] Bitmask dos sinalizadores usados para indicar as alterações sejam feitas para a rotina ociosa. Sinalizadores a seguir podem ser definidos em qualquer combinação:
    
  - FIRCCSEC: Uma alteração para o tempo associado a rotina ociosa, ou seja, uma alteração indicada pelo valor passado no parâmetro _csecIdle_ . 
      
  - FIRCIRO: Uma alteração para as opções para a rotina de ociosidade, ou seja, uma alteração indicada pelo valor passado no parâmetro _iroIdle_ . 
      
  - FIRCPFN: Uma alteração para o ponteiro de rotina ocioso, ou seja, uma alteração indicada pelo valor passado no parâmetro _pfnIdle_ . 
      
  - FIRCPRI: Uma alteração para a prioridade de rotina de ociosidade, ou seja, uma alteração indicada pelo valor passado no parâmetro _priIdle_ . 
      
  - FIRCPV: Uma alteração para o bloco de memória de rotina ocioso, ou seja, uma alteração indicada pelo valor passado no parâmetro _pvIdleParam_ . 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) : 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|**ChangeIdleRoutine** <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar. Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade. 
  

