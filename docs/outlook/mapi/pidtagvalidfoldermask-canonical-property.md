---
title: Propriedade canônica PidTagValidFolderMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagValidFolderMask
api_type:
- COM
ms.assetid: 83a44aee-5269-42a8-8078-4bc063bb6e29
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 925e0eb60d55349ded114b827b6ca67e3b5ac1ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360742"
---
# <a name="pidtagvalidfoldermask-canonical-property"></a>Propriedade canônica PidTagValidFolderMask

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask de sinalizadores que indicam a validade dos identificadores de entrada das pastas em um repositório de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_VALID_FOLDER_MASK  <br/> |
|Identificador:  <br/> |0x35DF  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Repositório de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Um identificador de entrada de pasta pode se tornar inválido se um usuário excluir a pasta ou se o repositório de mensagens ficar corrompido.
  
Um ou mais dos seguintes sinalizadores podem ser definidos para a bitmask: 
  
FOLDER_COMMON_VIEWS_VALID 
  
> A pasta Common views tem um identificador de entrada válido. ConFira **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md)).
    
FOLDER_FINDER_VALID 
  
> A pasta Finder tem um identificador de entrada válido. ConFira **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md)). 
    
FOLDER_IPM_INBOX_VALID 
  
> A pasta de recebimento de mensagem interpessoal (IPM) tem um identificador de entrada válido. Consulte [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md). 
    
FOLDER_IPM_OUTBOX_VALID 
  
> A pasta de saída IPM tem um identificador de entrada válido. ConFira **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)). 
    
FOLDER_IPM_SENTMAIL_VALID 
  
> A pasta Itens enviados IPM tem um identificador de entrada válido. ConFira **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
    
FOLDER_IPM_SUBTREE_VALID 
  
> A subárvore de pastas IPM tem um identificador de entrada válido. ConFira **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
FOLDER_IPM_WASTEBASKET_VALID 
  
> A pasta de itens excluídos IPM tem um identificador de entrada válido. ConFira **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)).
    
FOLDER_VIEWS_VALID 
  
> A pasta views tem um identificador de entrada válido. ConFira **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md)).
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

