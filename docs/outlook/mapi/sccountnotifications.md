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
ms.openlocfilehash: 923864c625cb032c3b351bb999ff7cc782eae588
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567164"
---
# <a name="sccountnotifications"></a>ScCountNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Determina o tamanho, em bytes, de uma matriz de notificações de evento e valida a memória associada a matriz.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _cntf_
  
> [in] Contagem de estruturas de [notificação](notification.md) na matriz indicado pelo parâmetro _rgntf_ . 
    
 _rgntf_
  
> [in] Ponteiro para a matriz de estruturas de **notificação** cujo tamanho é seja determinado. 
    
 _PCB_
  
> [out] Ponteiro opcional para o tamanho, em bytes, da matriz apontado pelo parâmetro _rgntf_ . Se for NULL, **ScCountNotifications** valida a matriz de notificações. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Contagem de determinada com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

Se NULL é passada no parâmetro _pcb_ , a função **ScCountNotifications** somente valida a matriz de notificações, mas nenhum contando é feito; Se um valor não-nulo é passado _pcb_, **ScCountNotifications** determina o tamanho da matriz e armazena a causa _pcb_. O parâmetro _pcb_ deve ser grande o suficiente para conter toda a matriz. 
  

