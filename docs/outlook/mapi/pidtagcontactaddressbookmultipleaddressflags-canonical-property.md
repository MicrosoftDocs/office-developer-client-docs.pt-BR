---
title: Propriedade canônica PidTagContactAddressBookMultipleAddressFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlags
api_type:
- HeaderDef
ms.assetid: ed3bc585-13f6-46a5-9e71-9c8513ddfc0a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b783a624ef5358a69d65dd52785b285db1a70df7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588668"
---
# <a name="pidtagcontactaddressbookmultipleaddressflags-canonical-property"></a>Propriedade canônica PidTagContactAddressBookMultipleAddressFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém os sinalizadores que indicam se os provedores dará suporte a email vários endereços por item de contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAGS  <br/> |
|Identificador:  <br/> |0x6625  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Catálogo de endereços de contatos  <br/> |
   
## <a name="remarks"></a>Comentários

Se os sinalizadores nessa propriedade forem TRUE, o provedor não inclui contatos sem endereços de email. Somente o endereço de email primário será atendido. Esta é uma propriedade em uma seção de perfil do catálogo de endereços de contatos.
  
## <a name="related-resources"></a>Recursos relacionados

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

