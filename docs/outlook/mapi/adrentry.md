---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19766161"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Aplica-se a**: Outlook 
  
Descreve as propriedades de zero ou mais que pertencem a um destinatário.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>Members

 **ulReserved1**
  
> Reservado; deve ser zero.
    
 **cValues**
  
> Contagem de propriedades da matriz de valores de propriedade apontado pelo membro **rgPropVals** . O membro **cValues** pode ser zero. 
    
 **rgPropVals**
  
> Ponteiro para uma matriz de valores de propriedade descrevendo as propriedades do destinatário. O membro **rgPropVals** pode ser NULL. 
    
## <a name="remarks"></a>Comentários

Uma estrutura **ADRENTRY** descreve as propriedades que pertencem a um único destinatário. As propriedades que geralmente são usadas para descrever um destinatário incluem o seguinte: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Quando um identificador de entrada ou a propriedade **PR_ENTRYID** aparece na matriz [SPropValue](spropvalue.md) para um destinatário, isto indica que o destinatário foi resolvido. Clientes chamar o método [IAddrBook::ResolveName](iaddrbook-resolvename.md) para certificar-se de que todos os destinatários na lista de destinatários de uma mensagem de saída foram resolvidos. Somente os destinatários resolvidos podem ser enviados com mensagens. 
  
 Estruturas **ADRENTRY** geralmente são combinadas para formar uma matriz para o membro **aEntries** de uma estrutura [ADRLIST](adrlist.md) . 
  
 Estruturas **ADRENTRY** e estruturas de [SRow](srow.md) são idênticas porque eles ambas contêm membro reservado, uma matriz de valores de propriedade e uma contagem dos valores na matriz. Enquanto **ADRENTRY** estruturas são combinadas para formar um membro de uma estrutura de **ADRLIST** **aEntries** , **SRow** estruturas são combinadas para formar o membro **aRow** uma estrutura [SRowSet](srowset.md) . Os dois tipos de estruturas seguem as mesmas regras de alocação, indicando que uma estrutura **SRowSet** que é recuperada no índice de conteúdo de um contêiner de catálogo de endereços pode ser convertida em uma estrutura **ADRLIST** e usada como está. 
  
Uma estrutura **ADRENTRY** pode estar vazia. Por exemplo, uma estrutura **ADRENTRY** que está contida na estrutura **ADRLIST** apontada pelo parâmetro _lppAdrList_ em uma chamada para **IAddrBook::Address** pode ser vazia quando um destinatário está sendo removido. 
  
Para obter mais informações sobre como alocar memória para as estruturas **ADRENTRY** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Confira também



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Estruturas MAPI](mapi-structures.md)

