---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360708"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ajusta um ponteiro dentro de uma matriz de notificação de eventos especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _CNTF_
  
> no Contagem de estruturas de [notificação](notification.md) na matriz indicada pelo parâmetro _rgntf_ . 
    
 _rgntf_
  
> no Ponteiro para a matriz de estruturas de **notificação** definindo notificações de eventos em que um ponteiro deve ser ajustado. 
    
 _pvBaseOld_
  
> no Ponteiro para o endereço base original da matriz indicada pelo parâmetro _rgntf_ . 
    
 _pvBaseNew_
  
> no O local para o qual o **ScRelocNotifications** grava o novo endereço base da matriz indicada pelo parâmetro _rgntf_ . 
    
 _PCB_
  
> bota Ponteiro para o tamanho, em bytes, da matriz indicada pelo parâmetro _pvBaseNew_ . 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> Um ponteiro foi ajustado com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

O parâmetro _PCB_ para a função **ScRelocNotifications** é opcional. 
  
## <a name="see-also"></a>Confira também



[ScRelocProps](screlocprops.md)

