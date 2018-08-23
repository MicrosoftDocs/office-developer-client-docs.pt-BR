---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ffc47e924b7a0f94db66adbffe01b2cdc619dc8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580730"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona ou move colunas para o início de uma tabela existente.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente.  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _lptbl_
  
> [in] Ponteiro para a tabela MAPI afetado.
    
 _lpproptagColumnsNew_
  
> [in] Ponteiro para uma estrutura **SPropTagArray** que contém uma matriz de marcas de propriedade para as propriedades sejam adicionados ou movidos para o início da tabela. 
    
 _lpAllocateBuffer_
  
> [in] Ponteiro para a função **MAPIAllocateBuffer** . Usado para alocar memória. 
    
 _lpFreeBuffer_
  
> [in] Ponteiro para a função **MAPIFreeBuffer** . Usado para liberar memória. 
    
## <a name="return-value"></a>Valor retornado

 **S_OK**
  
> A chamada foi bem-sucedida e das colunas especificadas foram movidas ou adicionadas.
    
## <a name="remarks"></a>Comentários

A função **HrAddColumns** é equivalente ao uso **HrAddColumnsEx** com _lpfnFilterColumns_ definido como NULL. 
  
## <a name="see-also"></a>Confira também



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

