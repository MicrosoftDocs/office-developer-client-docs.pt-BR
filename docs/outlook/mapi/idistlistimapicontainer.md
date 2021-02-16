---
title: IDistList IMAPIContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IDistList
api_type:
- COM
ms.assetid: bd8e1ddb-3027-428b-8964-81614f80282d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 463d81a6692b6071cada0ad22e7343020563e41c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431544"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece acesso a listas de distribuição em contêineres de agendas modificáveis. **IDistList** pode criar, copiar e excluir listas de distribuição, além de executar a resolução de nomes. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos de lista de distribuição  <br/> |
|Implementado por:  <br/> |Provedores de lista de endereços  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
|Identificador de interface:  <br/> |IID_IDistList  <br/> |
|Tipo de ponteiro:  <br/> |LPDISTLIST  <br/> |
|Modelo de transação:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

Essa interface não tem métodos exclusivos.
  
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

A interface **IDistList** herda de [IMAPIContainer](imapicontainerimapiprop.md) e inclui os mesmos métodos que os contêineres do livro de endereços. Portanto, como os métodos da interface **IDistList** são idênticos aos da interface [IABContainer,](iabcontainerimapicontainer.md) eles não são duplicados aqui. 
  
Uma lista de distribuição ou objeto que implementa **IDistList** é uma coleção de objetos de usuário de mensagens ou destinatários individuais. Uma lista de distribuição pode consistir em todos os objetos de usuário de mensagens ou algum usuário de mensagens e algumas listas de distribuição. 
  
Normalmente, há dois tipos de listas de distribuição:
  
- Listas de distribuição expandidas pelo sistema de mensagens subjacente. Esse tipo de lista tem um endereço, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e é tratado da mesma forma como se fosse um destinatário individual. 
    
- Listas de distribuição que existem em um contêiner local e são expandidas pelo aplicativo cliente.
    
As propriedades opcionais da lista de distribuição incluem o seguinte:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Observe que **PR_ADDRTYPE** é necessário, **mas PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) não é. Isso porque uma lista de distribuição sem um endereço de email ainda pode receber mensagens, mas sua lista de membros deve ser expandida. Se a **PR_ADDRTYPE** propriedade for definida como MAPIPDL, o MAPI executará a expansão. Se **PR_ADDRTYPE** for um valor diferente de MAPIPDL, o provedor de transporte executará a expansão. 
  
Para obter informações adicionais sobre como usar os métodos **IDistList,** consulte as entradas de referência para os métodos paralelos de **IABContainer**.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

