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
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
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
  
> Contagem de entradas na matriz especificada pelo membro **aEntries.** 
    
**aEntries**
  
> Matriz de [estruturas ADRENTRY,](adrentry.md) uma estrutura para cada destinatário. 
    
## <a name="remarks"></a>Comentários

Uma **estrutura ADRLIST** contém uma ou mais estruturas **ADRENTRY,** cada uma descrevendo as propriedades de um destinatário. Um destinatário pode ser não resolvido. Isso significa que não há um identificador de entrada em sua matriz de valores de propriedade. Um destinatário resolvido significa que a **propriedade PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) está incluída. Normalmente, os destinatários resolvidos também têm um endereço de email **PR_EMAIL_ADDRESS** propriedade ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). No entanto, o endereço de email não é obrigatório. **Estruturas ADRLIST** são usadas, por exemplo, para descrever a lista de destinatários de uma mensagem de saída e por MAPI para exibir as entradas no livro de endereços. 
  
**Estruturas ADRLIST** [assemelham-se a estruturas SRowSet](srowset.md) as estruturas usadas para representar linhas em tabelas. Na verdade, essas duas estruturas foram projetadas para que possam ser usadas de forma intercambiável. Ambos contêm uma matriz de estruturas que descrevem um grupo de propriedades e uma contagem dos valores na matriz. Enquanto na estrutura **ADRLIST,** a matriz contém estruturas [ADRENTRY,](adrentry.md) na estrutura **SRowSet** a matriz contém estruturas [SRow.](srow.md) **Estruturas ADRENTRY** e **SRow** são idênticas no layout. Como as estruturas **ADRLIST** e **SRowSet** seguem as mesmas regras de alocação, uma estrutura **SRowSet** recuperada do índice de um contêiner de um livro de endereços pode ser lançada em uma estrutura **ADRLIST** e usada como está. 
  
A ilustração a seguir mostra o layout de uma **estrutura ADRLIST.** 
  
**ADRLIST components**
  
![Componentes ADRLIST componentes](media/amapi_18.gif "ADRLIST")
  
As **partes ADRENTRY** e [SPropValue](spropvalue.md) em uma estrutura **ADRLIST** devem ser alocadas e liberadas independentemente das outras partes. Ou seja, cada **estrutura SPropValue** deve ser alocada individualmente depois que a memória para a estrutura **ADRENTRY** tiver sido alocada e liberada antes que a estrutura **ADRENTRY** seja liberada. Essa independência na manipulação da memória permite que destinatários e propriedades de destinatário individuais sejam adicionadas ou excluídas livremente da lista de endereços. 
  
As [funções MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) devem ser usadas para alocar e liberar a estrutura **ADRLIST** e todas as suas partes. 
  
Se uma lista de destinatários for muito grande para caber na memória, os clientes poderão chamar o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) para trabalhar com um subconjunto da lista. Os clientes não devem usar as caixas de diálogo comuns do livro de endereços nessa situação. 
  
Para obter mais informações sobre como alocar memória para estruturas **ADRENTRY,** consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Confira também

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Estruturas MAPI](mapi-structures.md)

