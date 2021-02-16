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
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421435"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve zero ou mais propriedades que pertencem a um destinatário.
  
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
  
> Contagem de propriedades na matriz de valores de propriedade apontada pelo **membro rgPropVals.** O **membro cValues** pode ser zero. 
    
 **rgPropVals**
  
> Ponteiro para uma matriz de valores de propriedade descrevendo as propriedades do destinatário. O **membro rgPropVals** pode ser NULL. 
    
## <a name="remarks"></a>Comentários

Uma **estrutura ADRENTRY** descreve as propriedades que pertencem a um único destinatário. As propriedades que normalmente são usadas para descrever um destinatário incluem o seguinte: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Quando um identificador de entrada **ou PR_ENTRYID** propriedade aparece na matriz [SPropValue](spropvalue.md) de um destinatário, isso indica que o destinatário foi resolvido. Os clientes chamam [o método IAddrBook::ResolveName](iaddrbook-resolvename.md) para garantir que todos os destinatários na lista de destinatários de uma mensagem de saída tenham sido resolvidos. Somente destinatários resolvidos podem ser enviados com mensagens. 
  
 **Estruturas ADRENTRY** são normalmente combinadas para formar uma matriz para o membro **aEntries** de uma [estrutura ADRLIST.](adrlist.md) 
  
 **Estruturas ADRENTRY** e [SRow](srow.md) são idênticas porque ambas contêm um membro reservado, uma matriz de valores de propriedade e uma contagem de valores na matriz. Enquanto as **estruturas ADRENTRY** são combinadas para formar o membro **aEntries** de uma estrutura **ADRLIST,** as estruturas **SRow** são combinadas para formar o membro **aRow** de uma [estrutura SRowSet.](srowset.md) Os dois tipos de estruturas seguem as mesmas regras de alocação, indicando que uma estrutura **SRowSet** recuperada do índice de um contêiner de um livro de endereços pode ser lançada em uma estrutura **ADRLIST** e usada como está. 
  
Uma **estrutura ADRENTRY** pode estar vazia. Por exemplo, uma estrutura **ADRENTRY** contida na estrutura **ADRLIST** apontada pelo parâmetro  _lppAdrList_ em uma chamada para **IAddrBook::Address** pode estar vazia quando um destinatário está sendo removido. 
  
Para obter mais informações sobre como alocar memória para estruturas **ADRENTRY,** consulte Gerenciando memória para [estruturas ADRLIST e SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Confira também



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[Estruturas MAPI](mapi-structures.md)

