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
ms.openlocfilehash: 5c634fe200dde4bfe6f190f8bfa9e5dfa0868db4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770509"
---
# <a name="srowset"></a>SRowSet

  
  
**Aplica-se a**: Outlook 
  
Contém uma matriz de estruturas de [SRow](srow.md) . Cada estrutura **SRow** descreve uma linha de uma tabela. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Macros relacionadas:  <br/> |[CbNewSRowSet](cbnewsrowset.md), [CbSRowSet](cbsrowset.md), [SizedSRowSet](sizedsrowset.md) <br/> |
   
```cpp
typedef struct _SRowSet
{
  ULONG cRows;
  SRow aRow[MAPI_DIM];
} SRowSet, FAR *LPSRowSet;

```

## <a name="members"></a>Members

 **Pássaros**
  
> Contagem de estruturas de **SRow** no membro **aRow** . 
    
 **aRow**
  
> Matriz de estruturas de **SRow** . Não há uma estrutura para cada linha da tabela. 
    
## <a name="remarks"></a>Comentários

Uma estrutura de **SRowSet** é usada para descrever a várias linhas de dados de uma tabela. Estruturas de **SRowSet** são usadas nos métodos de interface [IAddrBook](iaddrbookimapiprop.md), [ITableData](itabledataiunknown.md)e [IMAPITable](imapitableiunknown.md) , além das funções a seguir: 
  
- [HrQueryAllRows](hrqueryallrows.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
 Estruturas de **SRowSet** são definidas da mesma forma estruturas [ADRLIST](adrlist.md) para permitir que as linhas de uma tabela de destinatário e as entradas em uma lista de endereços a ser tratados da mesma. Estruturas de **SRowSet** e de estruturas **ADRLIST** podem ser passadas para os métodos como [IMessage::ModifyRecipients](imessage-modifyrecipients.md) e [IAddrBook::Address](iaddrbook-address.md). 
  
Além disso, as regras de alocação de memória para as estruturas de **SRowSet** são iguais às propriedades de estruturas **ADRLIST** . Resumindo, cada estrutura [SPropValue](spropvalue.md) na matriz apontada para pelo membro de cada linha na linha **lpProps** definir deve ser alocada separadamente usando [MAPIAllocateBuffer](mapiallocatebuffer.md). Cada estrutura de valor de propriedade também deve ser desalocada usando [MAPIFreeBuffer](mapifreebuffer.md) antes da desalocação de sua estrutura de **SRowSet** para que os ponteiros para as estruturas de **SPropValue** alocados não são perdidos. Uma linha do alocar memória podem então ser preservada e reutilizada fora do contexto da estrutura **SRowSet** . 
  
Para obter mais informações sobre como a memória para as estruturas de **SRowSet** deve ser alocada, consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Confira também



[ADRLIST](adrlist.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)


[Estruturas MAPI](mapi-structures.md)

