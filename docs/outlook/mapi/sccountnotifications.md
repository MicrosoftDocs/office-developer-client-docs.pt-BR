---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351367"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o tamanho, em bytes, de uma matriz de notificações de eventos e valida a memória associada à matriz.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _CNTF_
  
> no Contagem de estruturas de [notificação](notification.md) na matriz indicada pelo parâmetro _rgntf_ . 
    
 _rgntf_
  
> no Ponteiro para a matriz de estruturas de **notificação** cujo tamanho deve ser determinado. 
    
 _PCB_
  
> bota Ponteiro opcional para o tamanho, em bytes, da matriz apontada pelo parâmetro _rgntf_ . Se NULL, **ScCountNotifications** valida a matriz de notificações. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A contagem foi determinada com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

Se NULL for passado no parâmetro _PCB_ , a função **ScCountNotifications** validará apenas a matriz de notificações, mas nenhuma contagem será feita; se um valor não nulo for passado em _PCB_, **ScCountNotifications** determinará o tamanho da matriz e armazenará a _PCB_de causa. O parâmetro _PCB_ deve ser grande o suficiente para conter toda a matriz. 
  

