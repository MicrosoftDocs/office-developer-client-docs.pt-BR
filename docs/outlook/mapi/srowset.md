---
title: SRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRowSet
api_type:
- COM
ms.assetid: 7e3761be-afd6-46cb-9a08-25e9016c1241
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 63cef6ef2bb26e8b723c60fe01dd6771aa070ae8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341633"
---
# <a name="srowset"></a>SRowSet

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas [SRow](srow.md) . Cada estrutura **SRow** descreve uma linha de uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **Galinha**
  
> Contagem de estruturas **SRow** no membro **aRow** . 
    
 **aRow**
  
> Matriz de estruturas **SRow** . Há uma estrutura para cada linha na tabela. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **SRowSet** é usada para descrever várias linhas de dados de uma tabela. As estruturas **SRowSet** são usadas nos métodos de interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e IMAPITable, além das seguintes funções: [](imapitableiunknown.md) 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 As estruturas **SRowSet** são definidas da mesma forma que as estruturas [das ADRLIST](adrlist.md) para permitir que as linhas de uma tabela de destinatários e as entradas em uma lista de endereços sejam tratadas da mesma forma. Tanto estruturas **SRowSet** quanto estruturas **das ADRLIST** podem ser passadas para métodos como [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook:: address](iaddrbook-address.md). 
  
Além disso, as regras para a alocação de memória para estruturas **SRowSet** são as mesmas que as estruturas **das ADRLIST** . Para resumir, cada estrutura [SPropValue](spropvalue.md) na matriz apontada pelo membro **lpProps** de cada linha no conjunto de linhas deve ser alocaDa separadamente usando o [MAPIAllocateBuffer](mapiallocatebuffer.md). Cada estrutura de valor de propriedade também deve ser desalocada usando [MAPIFreeBuffer](mapifreebuffer.md) antes da desalocação de sua estrutura **SRowSet** para que os ponteiros para as estruturas **SPropValue** alocadas não sejam perdidos. A memória alocada de uma linha pode ser preservada e reutilizada fora do contexto da estrutura **SRowSet** . 
  
Para obter mais informações sobre como a memória para estruturas do **SRowSet** devem ser alocadas, consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Estruturas MAPI](mapi-structures.md)

