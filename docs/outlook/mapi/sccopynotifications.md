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
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357481"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um grupo de notificações de eventos para um único bloco de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parâmetros

 _CNTF_
  
> no Contagem de estruturas de [notificação](notification.md) na matriz indicada pelo parâmetro _rgntf_ . 
    
 _rgntf_
  
> no Ponteiro para uma matriz de estruturas de **notificação** que define as notificações de eventos a serem copiadas. 
    
 _pvDst_
  
> bota Ponteiro para as notificações retornadas. 
    
 _PCB_
  
> bota Ponteiro opcional para uma variável onde o tamanho, em bytes, da matriz apontada pelo parâmetro _rgntf_ é armazenado. Se não for nulo, o parâmetro _PCB_ será definido como o número de bytes armazenados no parâmetro _pvDst_ . 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> As notificações de eventos foram copiadas com êxito.
    
E_INVALIDARG
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

Se NULL for passado no parâmetro _PCB_ , nenhuma cópia será executada; se um valor não nulo é passado no _PCB_, a função **ScCopyNotifications** copia o tamanho da matriz e a própria matriz para um único bloco de memória. Se _PCB_ não for nulo, será definido como o número de bytes armazenados no parâmetro _pvDst_ . O parâmetro _pvDst_ deve ser grande o suficiente para conter toda a matriz. 
  

