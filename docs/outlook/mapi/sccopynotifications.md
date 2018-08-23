---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593351"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um grupo de notificações de evento para um único bloco de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _cntf_
  
> [in] Contagem de estruturas de [notificação](notification.md) na matriz indicado pelo parâmetro _rgntf_ . 
    
 _rgntf_
  
> [in] Ponteiro para uma matriz de estruturas de **notificação** , definindo as notificações de evento a ser copiado. 
    
 _pvDst_
  
> [out] Ponteiro para as notificações retornados. 
    
 _PCB_
  
> [out] Opcional ponteiro para uma variável onde o tamanho, em bytes, da matriz apontado pelo parâmetro _rgntf_ é armazenado. Se não for NULL, o parâmetro _pcb_ estiver definido como o número de bytes armazenado no parâmetro _pvDst_ . 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> Notificações de evento foram copiadas com êxito.
    
E_INVALIDARG
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

Se NULL é passada no parâmetro _pcb_ , cópia não é executada; Se um valor não-nulo é passado _pcb_, a função **ScCopyNotifications** copia o tamanho da matriz e do próprio conjunto para um único bloco de memória. Se _pcb_ não for nula, ela é definida como o número de bytes armazenado no parâmetro _pvDst_ . O parâmetro _pvDst_ deve ser grande o suficiente para conter toda a matriz. 
  

