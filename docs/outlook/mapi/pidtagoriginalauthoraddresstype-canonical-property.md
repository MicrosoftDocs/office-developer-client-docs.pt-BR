---
title: Propriedade canônica PidTagOriginalAuthorAddressType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorAddressType
api_type:
- COM
ms.assetid: 7cdedb1a-e441-469b-be50-2f18203eb30d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 596e416624fb6f2bf1fdaef64c2179feb7787815
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431411"
---
# <a name="pidtagoriginalauthoraddresstype-canonical-property"></a>Propriedade canônica PidTagOriginalAuthorAddressType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tipo de endereço do autor da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_AUTHOR_ADDRTYPE, PR_ORIGINAL_AUTHOR_ADDRTYPE_A, PR_ORIGINAL_AUTHOR_ADDRTYPE_W  <br/> |
|Identificador:  <br/> |0x0079  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Servidor  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são exemplos das propriedades de endereço do autor de uma mensagem. No primeiro envio da mensagem, o aplicativo cliente deve definir essa propriedade como o valor da propriedade **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)). Ela nunca é alterada quando a mensagem é encaminhada ou respondida.
  
As propriedades originais do autor permitem a preservação de informações de fora do domínio de mensagens local. Quando uma mensagem chega de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não são perdidas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

