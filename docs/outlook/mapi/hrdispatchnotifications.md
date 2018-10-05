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
ms.openlocfilehash: f4af3f2fd094942c48e02849c60f3e46acb1a5f7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385561"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Força expedir de todas as notificações na fila. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> Tem sido despachadas todas as notificações na fila.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION foi recebida.
    
MAPI_E_NOT_INITIALIZED
  
> MAPI não foi inicializado.
    
## <a name="remarks"></a>Comentários

A função **HrDispatchNotifications** faz com que o MAPI expedir todas as notificações que estão atualmente enfileiradas no mecanismo de notificação de MAPI sem esperar por uma expedição de mensagem. Isso pode ter um efeito vantajoso na utilização de memória. Para obter mais informações, consulte [forçando uma notificação](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Alguns aplicativos Aguarde uma mensagem de notificação em um loop de tempo limite usando o Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) e funções [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) . Em todos exceto as plataformas mais rápidas, tais aplicativos podem sofrer baixo desempenho ou bloqueio par de notificações. Usando **HrDispatchNotifications** não apenas reduz o código, mas melhora o desempenho. 
  

