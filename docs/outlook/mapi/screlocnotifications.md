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
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770355"
---
# <a name="screlocnotifications"></a>ScRelocNotifications

  
  
**Aplica-se a**: Outlook 
  
Ajusta um ponteiro dentro de uma matriz de notificação de evento especificado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] Contagem de estruturas de [notificação](notification.md) na matriz indicado pelo parâmetro _rgntf_ . 
    
 _rgntf_
  
> [in] Ponteiro para a matriz de estruturas de **notificação** , definindo as notificações de evento dentro do qual um ponteiro deve ser ajustada. 
    
 _pvBaseOld_
  
> [in] Ponteiro para o endereço base original da matriz indicado pelo parâmetro _rgntf_ . 
    
 _pvBaseNew_
  
> [in] A posição na qual **ScRelocNotifications** grava o novo endereço base da matriz indicado pelo parâmetro _rgntf_ . 
    
 _PCB_
  
> [out] Ponteiro para o tamanho, em bytes, da matriz indicado pelo parâmetro _pvBaseNew_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Um ponteiro foi ajustado com êxito.
    
MAPI_E_INVALID_PARAMETER
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

O parâmetro _pcb_ para a função **ScRelocNotifications** é opcional. 
  
## <a name="see-also"></a>Confira também



[ScRelocProps](screlocprops.md)

