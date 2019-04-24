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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342242"
---
# <a name="fnidle"></a>FNIDLE
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define uma rotina ociosa que o mecanismo de ociosidade de MAPI chama periodicamente de acordo com prioridade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
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
  
> no Ponteiro para um bloco de memória que o MAPI passa para a rotina de ociosidade cada vez que o chama. Esse ponteiro é passado para o mecanismo de ociosidade de MAPI no parâmetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Os dados no bloco de memória podem fornecer contexto para a chamada à rotina ociosa, como qual objeto operar ou o estado atual de uma operação demorada.
    
## <a name="return-value"></a>Valor de retorno

FALSE 
  
> Uma rotina ociosa com o protótipo **FNIDLE** sempre deve retornar false. 
    
## <a name="remarks"></a>Comentários

A funcionalidade específica da rotina ociosa é determinada pela implementação do aplicativo cliente ou provedor de serviços. 
  
O cliente ou provedor deve limitar o tempo de execução de cada Estado de uma rotina ociosa. Cada Estado deve realizar uma quantidade mínima de processamento, atualizar o estado atual nos dados de contexto apontados pelo _lpvContext_e retornar ao mecanismo de ociosidade de MAPI. 
  
O cliente ou provedor deve chamar a função MAPI [MAPIInitIdle](mapiinitidle.md) antes de poder registrar sua própria rotina ociosa com uma chamada para a função [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do FNIDLE: 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** aceitam como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  

