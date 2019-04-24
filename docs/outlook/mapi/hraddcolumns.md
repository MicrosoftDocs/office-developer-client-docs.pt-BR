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
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348192"
---
# <a name="hraddcolumns"></a>HrAddColumns

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona ou move colunas no início de uma tabela existente.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços.  <br/> |
   
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
  
> no Ponteiro para a tabela MAPI afetada.
    
 _lpproptagColumnsNew_
  
> no Ponteiro para uma estrutura **SPropTagArray** que contém uma matriz de marcas de propriedade para as propriedades a serem adicionadas ou movidas para o início da tabela. 
    
 _lpAllocateBuffer_
  
> no Ponteiro para a função **MAPIAllocateBuffer** . Usado para alocar memória. 
    
 _lpFreeBuffer_
  
> no Ponteiro para a função **MAPIFreeBuffer** . Usado para liberar memória. 
    
## <a name="return-value"></a>Valor de retorno

 **S_OK**
  
> A chamada foi bem-sucedida e as colunas especificadas foram movidas ou adicionadas.
    
## <a name="remarks"></a>Comentários

A função **HrAddColumns** é equivalente a usar **HrAddColumnsEx** com _lpfnFilterColumns_ definido como nulo. 
  
## <a name="see-also"></a>Confira também



[HrAddColumnsEx](hraddcolumnsex.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)

