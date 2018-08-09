---
title: HrDispatchNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDispatchNotifications
api_type:
- COM
ms.assetid: 42ec4266-67b9-416e-8b9b-163c95011626
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 28afa338b37e747ed441a8767981b7e63808e741
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766787"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Aplica-se a**: Outlook 
  
Força expedir de todas as notificações na fila. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Tem sido despachadas todas as notificações na fila.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION foi recebida.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI não foi inicializado.
    
## <a name="remarks"></a>Comentários

A função **HrDispatchNotifications** faz com que o MAPI expedir todas as notificações que estão atualmente enfileiradas no mecanismo de notificação de MAPI sem esperar por uma expedição de mensagem. Isso pode ter um efeito vantajoso na utilização de memória. Para obter mais informações, consulte [forçando uma notificação](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Alguns aplicativos Aguarde uma mensagem de notificação em um loop de tempo limite usando o Windows [PeekMessage](http://msdn.microsoft.com/en-us/library/ms644943.aspx) e funções [DispatchMessage](http://msdn.microsoft.com/en-us/library/ms644934.aspx) . Em todos exceto as plataformas mais rápidas, tais aplicativos podem sofrer baixo desempenho ou bloqueio par de notificações. Usando **HrDispatchNotifications** não apenas reduz o código, mas melhora o desempenho. 
  

