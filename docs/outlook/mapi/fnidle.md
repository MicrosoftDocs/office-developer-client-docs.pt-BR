---
title: FNIDLE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FNIDLE
api_type:
- COM
ms.assetid: f6b31bb4-69dd-43de-b62b-abfa99557641
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 534f4da15bba5f38bec4cde91206694f8691cbc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412377"
---
# <a name="fnidle"></a>FNIDLE
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma rotina ociosa que o mecanismo ocioso MAPI chama periodicamente de acordo com a prioridade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Função definida implementada por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
|Tipo de ponteiro correspondente:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parâmetros

 _lpvContext_
  
> [in] Ponteiro para um bloco de memória que o MAPI passa para a rotina ociosa sempre que o chama. Esse ponteiro é passado para o mecanismo ocioso MAPI no parâmetro  _pvIdleParam_ pelo [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Os dados no bloco de memória podem fornecer contexto para a chamada para a rotina ociosa, como qual objeto operar ou o estado atual de uma operação demorada.
    
## <a name="return-value"></a>Valor de retorno

FALSE 
  
> Uma rotina ociosa com o **protótipo FNIDLE** sempre deve retornar FALSE. 
    
## <a name="remarks"></a>Comentários

A funcionalidade específica da rotina ociosa é determinada pela implementação do aplicativo cliente ou do provedor de serviços. 
  
O cliente ou provedor deve limitar o tempo de execução de cada estado de uma rotina ociosa. Cada estado deve executar uma quantidade mínima de processamento, atualizar o estado atual nos dados de contexto apontados por  _lpvContext_ e retornar ao mecanismo ocioso MAPI. 
  
O cliente ou provedor deve chamar a função [MAPIInitIdle](mapiinitidle.md) antes de registrar sua própria rotina ociosa com uma chamada para a função [FtgRegisterIdleRoutine.](ftgregisteridleroutine.md) 
  
As funções a seguir lidam com o mecanismo ocioso MAPI e com rotinas ociosas com base no protótipo de função FNIDLE: 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina ociosa registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina ociosa registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou reabilitar uma rotina ociosa registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem habilita-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo ocioso MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine** e **EnableIdleRoutine** levam como parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas em primeiro plano da plataforma ficam ociosas, o mecanismo ocioso MAPI chama a rotina ociosa de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  

