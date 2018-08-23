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
ms.openlocfilehash: fd9a91b089bb06e6dfe34a1a144245d404adb270
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569222"
---
# <a name="mapiinitidle"></a>MAPIInitIdle

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
LONG MAPIInitIdle(
  LPVOID lpvReserved
);
```

## <a name="parameters"></a>Parâmetros

 _lpvReserved_
  
> [in] Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

A função **MAPIInitIdle** retorna zero se a inicialização é bem-sucedida e 1, caso contrário. Se **MAPIInitIdle** for chamado várias vezes, todas as chamadas adicionais êxito, mas são ignoradas, exceto to incrementa a contagem de referência. 
  
## <a name="remarks"></a>Comentários

Um aplicativo cliente ou um provedor de serviços deve chamar **MAPIInitIdle** antes de chamar qualquer outra função de mecanismo ocioso. 
  
Todas as chamadas para **MAPIInitIdle** devem ser iguais por uma chamada subsequente para [MAPIDeInitIdle](mapideinitidle.md)ou o mecanismo de ocioso é deixado em execução para o aplicativo de chamada. 
  
As seguintes funções lidam com o mecanismo de ociosidade de MAPI e com ociosas rotinas com base no protótipo de função [FNIDLE](fnidle.md) : 
  
|**Função de rotina ociosa**|**Uso**|
|:-----|:-----|
|[ChangeIdleRoutine](changeidleroutine.md) <br/> |Altera as características de uma rotina de ociosidade registrada.  <br/> |
|[DeregisterIdleRoutine](deregisteridleroutine.md) <br/> |Remove uma rotina de ociosidade registrada do sistema MAPI.  <br/> |
|[EnableIdleRoutine](enableidleroutine.md) <br/> |Desativa ou ativa novamente uma rotina de ociosidade registrada sem removê-lo a partir do sistema MAPI.  <br/> |
|[FtgRegisterIdleRoutine](ftgregisteridleroutine.md) <br/> |Adiciona uma rotina de ociosidade ao sistema de MAPI, com ou sem ativá-lo.  <br/> |
|[MAPIDeInitIdle](mapideinitidle.md) <br/> |Desliga o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
|**MAPIInitIdle** <br/> |Inicializa o mecanismo de ociosidade de MAPI para o aplicativo de chamada.  <br/> |
   
Quando todas as tarefas de primeiro plano para a plataforma ficam ociosas, o mecanismo de ociosidade de MAPI chama a rotina de ocioso de prioridade mais alta que está pronta para executar. Não há nenhuma garantia de chamar ordem entre as rotinas de ociosidade da mesma prioridade. 
  

