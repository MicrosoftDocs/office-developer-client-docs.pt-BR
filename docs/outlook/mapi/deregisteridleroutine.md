---
title: DeregisterIdleRoutine
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DeregisterIdleRoutine
api_type:
- COM
ms.assetid: a8ada6fe-9963-4c25-b4b4-db77f9517368
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 62231a900dbe01ebe1e848355226c0589072cd42
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404558"
---
# <a name="deregisteridleroutine"></a>DeregisterIdleRoutine

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Remove uma rotina [ociosa baseada em FNIDLE](fnidle.md) do sistema MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
VOID DeregisterIdleRoutine(
  FTG ftg
);
```

## <a name="parameters"></a>Parâmetros

 _ftg_
  
> [in] Marca de função que identifica a rotina ociosa a ser removida.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Qualquer tarefa em um aplicativo cliente ou provedor de serviços pode desregister qualquer rotina ociosa para a qual tenha um parâmetro  _ftg_ válido. Em particular, uma rotina ociosa pode se desregister. 
  
As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md) 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina ociosa registrada.  <br/> |
|**DeregisterIdleRoutine** <br/> |Remove uma rotina ociosa registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
   
 **ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  
Depois que a rotina ociosa for desregisterada, o mecanismo ocioso não a chamará novamente. Qualquer implementação que chame **DeregisterIdleRoutine** deve desalocar todos os blocos de memória para os quais ele passou ponteiros para o mecanismo ocioso usar em sua chamada original para a função **FtgRegisterIdleRoutine.** 
  

