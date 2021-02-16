---
title: SRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRow
api_type:
- COM
ms.assetid: 369c2d5c-8c2b-4314-9cb2-aaa89580aa2b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2e75bc6f8e14258787a6c9d80dfbf6334ec698b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410431"
---
# <a name="srow"></a>SRow

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma linha de uma tabela que contém propriedades selecionadas para um objeto específico. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRow
{
  ULONG ulAdrEntryPad;
  ULONG cValues;
  LPSPropValue lpProps;
} SRow, FAR *LPSRow;

```

## <a name="members"></a>Members

**ulAdrEntryPad**
  
> Preenchimento de bytes para alinhar corretamente os valores de propriedade apontados pelo **membro lpProps.** 
    
**cValues**
  
> Contagem de valores de propriedade apontados **por lpProps**. 
    
**lpProps**
  
> Ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) que descrevem os valores de propriedade para as colunas na linha. 
    
## <a name="remarks"></a>Comentários

Uma **estrutura SRow** descreve uma linha em uma tabela. Ele está incluído na estrutura [TABLE_NOTIFICATION](table_notification.md) que acompanha uma notificação de tabela. 
  
**As estruturas SRow** são usadas nos seguintes métodos: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData : IUnknown](itabledataiunknown.md) (muitos métodos) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Quando mais de uma linha precisa ser descrita, uma [estrutura SRowSet](srowset.md) é usada. Uma **estrutura SRowSet** contém uma matriz de **estruturas SRow** e uma contagem de estruturas na matriz. 
  
A ilustração a seguir mostra a relação entre uma **SRow** e uma **estrutura de dados SRowSet.** 
  
**Relationship between SRow and SRowSet**
  
![Relação entre SRow e SRowSet](media/amapi_17.gif "Relationship entre SRow e SRowSet")
  
**As estruturas SRow** são definidas da mesma forma que [as estruturas ADRENTRY.](adrentry.md) Portanto, uma linha de uma tabela de destinatários e uma entrada em uma lista de endereços podem ser tratadas da mesma forma. 
  
Para obter informações sobre como a memória para estruturas **SRow** deve ser alocada, consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Confira também

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Estruturas MAPI](mapi-structures.md)
- [Gerenciando memória para estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

