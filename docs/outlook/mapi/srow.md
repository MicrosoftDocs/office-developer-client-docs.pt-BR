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
ms.openlocfilehash: 56bf1366cdd44fac185277280d2e8ab80c644c45
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579120"
---
# <a name="srow"></a>SRow

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma linha de uma tabela que contém as propriedades selecionadas para um objeto específico. 
  
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
  
> Preenchimento bytes para alinhar adequadamente os valores de propriedade apontado pelo membro **lpProps** . 
    
**cValues**
  
> Contagem de valores de propriedade apontado pela **lpProps**. 
    
**lpProps**
  
> Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) que descrevem os valores de propriedade para as colunas na linha. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **SRow** descreve uma linha em uma tabela. Ele está incluído na estrutura [TABLE_NOTIFICATION](table_notification.md) que acompanha uma notificação de tabela. 
  
Estruturas de **SRow** são usadas nos seguintes métodos: 
  
- [IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
    
- [IAddrBook::SetSearchPath](iaddrbook-setsearchpath.md)
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)
    
- [IMAPITable::ExpandRow](imapitable-expandrow.md)
    
- [ITableData: IUnknown](itabledataiunknown.md) (muitos métodos) 
    
- [FBadRowSet](fbadrowset.md)
    
- [FreeProws](freeprows.md)
    
- [HrQueryAllRows](hrqueryallrows.md)
    
Quando mais de uma linha precisa ser descrito, uma estrutura de [SRowSet](srowset.md) é usada. Uma estrutura **SRowSet** contém uma matriz de estruturas de **SRow** e uma contagem de estruturas na matriz. 
  
A ilustração a seguir mostra a relação entre um **SRow** e uma estrutura de dados **SRowSet** . 
  
**Relationship between SRow and SRowSet**
  
![Relação entre SRow e SRowSet] (media/amapi_17.gif "Relação entre SRow e SRowSet")
  
Estruturas de **SRow** são definidas iguais [ADRENTRY](adrentry.md) estruturas. Portanto, uma linha de uma tabela de destinatário e uma entrada em uma lista de endereços pode ser tratados da mesma. 
  
Para obter informações sobre como a memória para as estruturas de **SRow** deve ser alocada, consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Confira também

- [ADRENTRY](adrentry.md)
- [SPropValue](spropvalue.md)
- [SRowSet](srowset.md)
- [TABLE_NOTIFICATION](table_notification.md)
- [Estruturas MAPI](mapi-structures.md)
- [Gerenciar memória das estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md)

