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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: b2d3dce7835f92d9ad78f7d8837e655fdd8fd412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766149"
---
# <a name="adrlist"></a>ADRLIST

**Aplica-se a**: Outlook 
  
Descreve as propriedades de zero ou mais que pertencem a um ou mais destinatários. 
  
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

## <a name="members"></a>Membros

**cEntries**
  
> Contagem de entradas na matriz especificada pelo membro **aEntries** . 
    
**aEntries**
  
> Matriz de estruturas [ADRENTRY](adrentry.md) , uma estrutura de cada destinatário. 
    
## <a name="remarks"></a>Coment�rios

Uma estrutura **ADRLIST** contém uma ou mais estruturas **ADRENTRY** , cada uma delas descreve as propriedades de um destinatário. Um destinatário pode ser não resolvido. Isso significa que ele está faltando um identificador de entrada na sua matriz de valores de propriedade. Um destinatário resolvido significa que o **PR\_ENTRYID** propriedade ([PidTagEntryId](pidtagentryid-canonical-property.md)) esteja incluída. Geralmente, destinatários resolvidos também têm um email a propriedade **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) de endereços. No entanto, o endereço de email não é necessário. Estruturas **ADRLIST** são usadas, por exemplo, para descrever a lista de destinatários para uma mensagem de saída e por MAPI para exibir as entradas no catálogo de endereços. 
  
Estruturas **ADRLIST** assemelhar [SRowSet](srowset.md) estruturas as estruturas usadas para representar as linhas em tabelas. Na verdade, essas duas estruturas foram projetadas para que possa ser usados de forma intercambiável. Ambos contêm uma matriz de estruturas que descrevem um grupo de propriedades e uma contagem dos valores na matriz. Enquanto na estrutura de **ADRLIST** , a matriz contém estruturas [ADRENTRY](adrentry.md) , na estrutura de **SRowSet** a matriz contém estruturas [SRow](srow.md) . Estruturas **ADRENTRY** e estruturas de **SRow** são idênticas em layout. Como **ADRLIST** e **SRowSet** estruturas seguem as mesmas regras de alocação, uma estrutura **SRowSet** que é recuperada no índice de conteúdo de um contêiner de catálogo de endereços pode ser convertida em uma estrutura **ADRLIST** e usada como está. 
  
A ilustração a seguir mostra o layout de uma estrutura **ADRLIST** . 
  
**Componentes ADRLIST**
  
![Componentes ADRLIST] (media/amapi_18.gif "Componentes ADRLIST")
  
As partes **ADRENTRY** e [SPropValue](spropvalue.md) em uma estrutura **ADRLIST** devem ser alocadas e liberadas independentemente das outras partes. Ou seja, cada estrutura **SPropValue** deve ser alocada individualmente depois que a memória para a estrutura de **ADRENTRY** foi alocada e liberada antes que a estrutura **ADRENTRY** é liberada. Essa independência na manipulação de memória permite que os destinatários e propriedades de destinatário individuais livremente sejam adicionados ou excluídos da lista de endereços. 
  
As funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIFreeBuffer](mapifreebuffer.md) devem ser usadas para alocar e liberar a estrutura **ADRLIST** e todas as suas partes. 
  
Se uma lista de destinatários é muito grande para caber na memória, clientes podem chamar o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) para trabalhar com um subconjunto da lista. Os clientes não devem usar as caixas de diálogo comuns do endereço livro nesta situação. 
  
Para obter mais informações sobre como alocar memória para as estruturas **ADRENTRY** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Confira também

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [Estruturas MAPI](mapi-structures.md)

