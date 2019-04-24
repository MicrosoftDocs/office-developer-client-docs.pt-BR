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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348094"
---
# <a name="hrdispatchnotifications"></a>HrDispatchNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Força a expedição de todas as notificações em fila. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrDispatchNotifications(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> Todas as notificações em fila foram despachadas.
    
MAPI_E_USER_CANCEL
  
> WM_QUIT, WM_QUERYENDSESSION ou WM_ENDSESSION foi recebida.
    
MAPI_E_NOT_INITIALIZED
  
> O MAPI não foi inicializado.
    
## <a name="remarks"></a>Comentários

A função **HrDispatchNotifications** faz com que o MAPI envie todas as notificações que estão atualmente enfileiradas no mecanismo de notificação MAPI sem esperar por uma expedição de mensagem. Isso pode ter um efeito benéfico sobre a utilização da memória. Para obter mais informações, consulte [forçar uma notificação](forcing-a-notification.md). 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Alguns aplicativos esperam uma mensagem de notificação em um loop de tempo de espera usando as funções do Windows [PeekMessage](https://msdn.microsoft.com/library/ms644943.aspx) e do [DispatchMessage](https://msdn.microsoft.com/library/ms644934.aspx) . Em todas as plataformas, exceto as mais rápidas, esses aplicativos podem experimentar um desempenho ruim ou até mesmo bloqueio de notificações. O uso do **HrDispatchNotifications** não apenas reduz o código, mas melhora o desempenho. 
  

