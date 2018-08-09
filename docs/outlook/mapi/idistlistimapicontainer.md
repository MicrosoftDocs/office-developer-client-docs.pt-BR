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
ms.openlocfilehash: 7fee3c84d6a4d4a94397f5197f45637b0c7dd2be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766925"
---
# <a name="idistlist--imapicontainer"></a>IDistList : IMAPIContainer

  
  
**Aplica-se a**: Outlook 
  
Fornece acesso às listas de distribuição no endereço modificável contêineres de catálogo. **IDistList** pode criar, copiar e excluir listas de distribuição, além de executar a resolução de nomes. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de lista de distribuição  <br/> |
|Implementada por:  <br/> |Provedores de catálogo de endereços  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IDistList  <br/> |
|Tipo de ponteiro:  <br/> |LPDISTLIST  <br/> |
|Modelo de transação:  <br/> |Transacionadas  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

Essa interface não tem quaisquer métodos exclusivos.
  
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

A interface **IDistList** herda de [IMAPIContainer](imapicontainerimapiprop.md) e inclui os mesmos métodos como recipientes do catálogo de endereços. Portanto, como os métodos da interface **IDistList** são idênticos da interface [IABContainer](iabcontainerimapicontainer.md) , eles não são duplicados aqui. 
  
Uma lista de distribuição ou um objeto que implementa **IDistList** é uma coleção de objetos de usuário de mensagens ou destinatários individuais. Uma lista de distribuição pode consistir em todos os objetos de usuário de mensagens, ou alguns usuários de mensagens e algumas listas de distribuição. 
  
Geralmente, há dois tipos de listas de distribuição:
  
- Listas de distribuição expandidas pelo sistema de mensagens subjacente. Esse tipo de lista possui um endereço, **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e é tratada da mesma como se fosse um destinatário individual. 
    
- Listas de distribuição que existem em um contêiner de local e são expandidas pelo aplicativo cliente.
    
Propriedades da lista de distribuição opcionais incluem o seguinte:
  
- **PR_LAST_MODIFICATION_TIME** ([PidTagLastModificationTime](pidtaglastmodificationtime-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) 
    
- **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) 
    
Observe que **PR_ADDRTYPE** é obrigatório, mas **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) não está. Isso acontece porque sem um endereço de email de uma lista de distribuição ainda poderá receber mensagens, mas sua lista de membros deve ser expandida. Se a propriedade **PR_ADDRTYPE** é definida como MAPIPDL, MAPI realiza a expansão. Se **PR_ADDRTYPE** for um valor diferente de MAPIPDL, o provedor de transporte executa a expansão. 
  
Para obter informações adicionais sobre como usar os métodos **IDistList** , consulte as entradas de referência para os métodos paralelas do **IABContainer**.
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

