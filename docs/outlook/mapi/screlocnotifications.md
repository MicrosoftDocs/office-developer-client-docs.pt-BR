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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415198"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Ajusta um ponteiro dentro de uma matriz de notificação de evento especificada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
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

 _cntf_
  
> [in] Contagem de [estruturas](notification.md) NOTIFICATION na matriz indicada pelo _parâmetro rgntf._ 
    
 _rgntf_
  
> [in] Ponteiro para a matriz de estruturas **notification** definindo notificações de evento dentro da qual um ponteiro deve ser ajustado. 
    
 _pvBaseOld_
  
> [in] Ponteiro para o endereço base original da matriz indicado pelo _parâmetro rgntf._ 
    
 _pvBaseNew_
  
> [in] O local no qual **ScRelocNotifications** grava o novo endereço base da matriz indicado pelo _parâmetro rgntf._ 
    
 _pcb_
  
> [out] Ponteiro para o tamanho, em bytes, da matriz indicada pelo _parâmetro pvBaseNew._ 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> Um ponteiro foi ajustado com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

O  _parâmetro pcb_ para a **função ScRelocNotifications** é opcional. 
  
## <a name="see-also"></a>Confira também



[ScRelocProps](screlocprops.md)

