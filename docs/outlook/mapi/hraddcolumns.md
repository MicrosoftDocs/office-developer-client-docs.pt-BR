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
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766759"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Aplica-se a**: Outlook 
  
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

