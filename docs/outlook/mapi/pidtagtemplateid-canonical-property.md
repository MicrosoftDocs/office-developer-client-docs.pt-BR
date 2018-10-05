---
title: Propriedade canônica PidTagTemplateid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTemplateid
api_type:
- COM
ms.assetid: 1a418c76-ebc7-47f2-ac91-797162e6e099
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96bcd15606771bd112568ad94133507ab14b2bcd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396390"
---
# <a name="pidtagtemplateid-canonical-property"></a>Propriedade canônica PidTagTemplateid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), expressado como um formato de ID de entrada permanente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TEMPLATEID  <br/> |
|Identificador:  <br/> |0x3902  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Catálogo de endereços MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esse valor deve estar presente para todos os objetos de catálogo de endereços em um servidor de nome serviço provedor NSPI (Interface), seu nome distinto (DN) deve corresponder ao valor de **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) e seu DN deve seguir o formato do DN especificação determinada para o tipo de objeto. 
  
Essa propriedade não está presente nos objetos em um catálogo de endereços offline.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

