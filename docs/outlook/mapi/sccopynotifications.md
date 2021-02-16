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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435919"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um grupo de notificações de eventos para um único bloco de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
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

 _cntf_
  
> [in] Contagem de [estruturas](notification.md) NOTIFICATION na matriz indicada pelo _parâmetro rgntf._ 
    
 _rgntf_
  
> [in] Ponteiro para uma matriz de **estruturas NOTIFICATION** definindo as notificações de evento a serem copiadas. 
    
 _pvDst_
  
> [out] Ponteiro para as notificações retornadas. 
    
 _pcb_
  
> [out] Ponteiro opcional para uma variável onde o tamanho, em bytes, da matriz apontado pelo  _parâmetro rgntf_ é armazenado. Se não for NULL, o _parâmetro pcb_ será definido como o número de bytes armazenados no _parâmetro pvDst._ 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> As notificações de evento foram copiadas com êxito.
    
E_INVALIDARG
  
> Uma notificação inválida foi encontrada.
    
## <a name="remarks"></a>Comentários

Se NULL for passado no parâmetro  _pcb,_ nenhuma cópia será executada; se um valor não nulo for passado em  _pcb_, a função **ScCopyNotifications** copia o tamanho da matriz e a matriz em si para um único bloco de memória. Se _pcb_ não for NULL, ele será definido como o número de bytes armazenados no _parâmetro pvDst._ O  _parâmetro pvDst_ deve ser grande o suficiente para conter toda a matriz. 
  

