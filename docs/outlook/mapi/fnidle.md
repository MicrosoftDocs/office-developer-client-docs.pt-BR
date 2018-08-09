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
ms.openlocfilehash: bf1a84a1f305580fc9d9085753ab7eb5c62b8aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766585"
---
# <a name="fnidle"></a>FNIDLE
 
**Aplica-se a**: Outlook 
  
Define uma rotina de ociosidade chamada pelo mecanismo de ociosidade de MAPI periodicamente de acordo com a prioridade. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Função definido implementada por:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
|Tipo de ponteiro correspondente:  <br/> |PFNIDLE  <br/> |
   
```cpp
BOOL (STDAPICALLTYPE FNIDLE)(
  LPVOID lpvContext
);
```

## <a name="parameters"></a>Parâmetros

 _lpvContext_
  
> [in] Ponteiro para um bloco de memória que MAPI passa para a rotina ociosa horário ele chama a ele. Esse ponteiro é passado para o mecanismo de ociosidade de MAPI no parâmetro _pvIdleParam_ por [FtgRegisterIdleRoutine](ftgregisteridleroutine.md). Os dados no bloco de memória poderá fornecer contexto para a chamada para a rotina ociosa, como o objeto a ser operado, ou o estado atual de uma operação demorada.
    
## <a name="return-value"></a>Valor retornado

FALSO 
  
> Uma rotina de ociosidade com o protótipo **FNIDLE** deve sempre retornam FALSE. 
    
## <a name="remarks"></a>Comentários

A funcionalidade específica de rotina ociosa é determinada Implementando o aplicativo cliente ou provedor de serviços. 
  
O cliente ou o provedor deverá limitar o tempo de execução de cada estado de uma rotina de ocioso. Cada estado deve realizar uma quantidade mínima de processamento, atualize o estado atual nos dados de contexto apontados pela _lpvContext_e retornar ao mecanismo de ociosidade de MAPI. 
  
O cliente ou o provedor deve chamar a função MAPI [MAPIInitIdle](mapiinitidle.md) para que ele possa registrar sua própria rotina ociosa com uma chamada para a função [FtgRegisterIdleRoutine](ftgregisteridleroutine.md) . 
  
As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função FNIDLE: 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|[MAPIInitIdle](mapiinitidle.md) <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
**ChangeIdleRoutine**, **DeregisterIdleRoutine**e **EnableIdleRoutine** tomar como um parâmetro de entrada a marca de função retornada por **FtgRegisterIdleRoutine**. 
  
Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar. Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade. 
  

