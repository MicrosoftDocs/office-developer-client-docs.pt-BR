---
title: MAPIDeInitIdle
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIDeInitIdle
api_type:
- COM
ms.assetid: f7b04486-bc48-4ba4-9f35-f021e06124bf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 74bba3ea9982838f0d010bbf106c1132df1c2c25
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408205"
---
# <a name="mapideinitidle"></a>MAPIDeInitIdle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
void MAPIDeInitIdle( void );
```

## <a name="parameters"></a>Parâmetros

Nenhum. 
  
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou provedor de serviços deve chamar **MAPIDeInitIdle** quando ele não precisar mais do mecanismo ocioso, por exemplo, quando estiver prestes a parar o processamento. 
  
Cada chamada para [MAPIInitIdle](mapiinitidle.md) deve ser correspondida por uma chamada subsequente para **MAPIDeInitIdle**ou o mecanismo de ociosidade é deixado em execução para o aplicativo de chamada. 
  
As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com rotinas ociosas com base no protótipo de função do [FNIDLE](fnidle.md) : 
  
|**Função de rotina ociosa**|**Usage**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desabilita ou habilita novamente uma rotina de ociosidade registrada sem removê-la do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina ociosa ao sistema MAPI, com ou sem ativá-la.  <br/> |
|**MAPIDeInitIdle** <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
Quando todas as tarefas de primeiro plano para a plataforma ficarem ociosas, o mecanismo de ociosidade de MAPI chamará a rotina de ociosidade de prioridade mais alta que está pronta para ser executada. Não há garantia de ordem de chamada entre rotinas ociosas da mesma prioridade. 
  

