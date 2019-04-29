---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415912"
---
# <a name="adrlist"></a>ADRLIST

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve zero ou mais propriedades que pertencem a um ou mais destinatários. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Macros relacionadas:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Contagem de entradas na matriz especificada pelo membro **aEntries** . 
    
**aEntries**
  
> Matriz de estruturas [ADRENTRY](adrentry.md) , uma estrutura para cada destinatário. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **das ADRLIST** contém uma ou mais estruturas **ADRENTRY** , cada uma descrevendo as propriedades de um destinatário. Um destinatário pode ser não resolvido. Isso significa que não há um identificador de entrada em sua matriz de valores de propriedade. Um destinatário resolvido significa que a **propriedade\_PR EntryID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) está incluída. Normalmente, os destinatários resolvidos também têm um endereço de email a propriedade **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). No enTanto, o endereço de email não é necessário. As estruturas **das ADRLIST** são usadas, por exemplo, para descrever a lista de destinatários para uma mensagem de saída e por MAPI para exibir as entradas no catálogo de endereços. 
  
Estruturas **das ADRLIST** se assemelham a estruturas [SRowSet](srowset.md) as estruturas usadas para representar linhas em tabelas. Na verdade, essas duas estruturas são projetadas para que possam ser usadas de forma intercambiável. Ambas contêm uma matriz de estruturas que descreve um grupo de propriedades e uma contagem dos valores na matriz. Enquanto na estrutura **das ADRLIST** , a matriz contém estruturas [ADRENTRY](adrentry.md) , na estrutura **SRowSet** , a matriz contém estruturas [SRow](srow.md) . Estruturas **ADRENTRY** e estruturas **SRow** são idênticas no layout. Como as estruturas **das ADRLIST** e **SRowSet** seguem as mesmas regras de alocação, uma estrutura **SRowSet** que é recuperada da tabela de conteúdo de um contêiner de catálogo de endereços pode ser convertida para uma estrutura **das ADRLIST** e usada como está. 
  
A ilustração a seguir mostra o layout de uma estrutura **das ADRLIST** . 
  
**ADRLIST components**
  
![Componentes do das ADRLIST] (media/amapi_18.gif "Componentes do das ADRLIST")
  
As partes **ADRENTRY** e [SPropValue](spropvalue.md) em uma estrutura **das ADRLIST** devem ser alocadas e liberadas independentemente das outras partes. Ou seja, cada estrutura **SPropValue** deve ser alocada individualmente após a memória para a estrutura **ADRENTRY** ter sido alocada e liberada antes da liberação da estrutura **ADRENTRY** . Essa independência no tratamento de memória permite que os destinatários e as propriedades de destinatário individuais sejam adicionados ou excluídos livremente da lista de endereços. 
  
As funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) devem ser usadas para alocar e liberar a estrutura do **das ADRLIST** e todas as suas partes. 
  
Se uma lista de destinatários for muito grande para caber na memória, os clientes podem chamar o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) para trabalhar com um subconjunto da lista. Os clientes não devem usar as caixas de diálogo comuns do catálogo de endereços nessa situação. 
  
Para obter mais informações sobre como alocar memória para estruturas **ADRENTRY** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Confira também

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Estruturas MAPI](mapi-structures.md)

