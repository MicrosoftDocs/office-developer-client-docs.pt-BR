---
title: MAPIInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIInitIdle
api_type:
- COM
ms.assetid: b6de7c6a-f2e7-4248-adea-d354924a8bbf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b07c40882c0b9974c71eeb03123e7025b948a75e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432440"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parâmetros

 _lpvReserved_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

A **função MAPIInitIdle** retornará zero se a inicialização for bem-sucedida e 1 caso contrário. Se **MAPIInitIdle** for chamado várias vezes, todas as chamadas adicionais serão bem-sucedidas, mas serão ignoradas, exceto para incrementar a contagem de referência. 
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou provedor de serviços deve chamar **MAPIInitIdle** antes de chamar qualquer outra função de mecanismo ocioso. 
  
Cada chamada para **MAPIInitIdle** deve ser a mesma de uma chamada subsequente para [MAPIDeInitIdle](mapideinitidle.md)ou o mecanismo ocioso é deixado em execução para o aplicativo de chamada. 
  
As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de [função FNIDLE:](fnidle.md) 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina ociosa registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina ociosa registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
|**MAPIInitIdle** <br/> |Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
   
Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  

