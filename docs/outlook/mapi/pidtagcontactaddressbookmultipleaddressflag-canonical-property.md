---
title: Propriedade canônica PidTagContactAddressBookMultipleAddressFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContactAddressBookMultipleAddressFlag
api_type:
- HeaderDef
ms.assetid: aefc34c5-1beb-44cf-a455-90f466e157ce
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6fabb03d552f195c200b0ecbd8fd69f470c0e1fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344888"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propriedade canônica PidTagContactAddressBookMultipleAddressFlag

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um sinalizador que é TRUE quando o provedor dá suporte a vários endereços de email por item de contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificador:  <br/> |0x6614  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Catálogo de endereços de contatos  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for TRUE, o provedor não permitirá contatos sem endereços de email. Se for FALSE, o provedor mostrará todos os contatos, tenha ou não um endereço de email principal. Somente o endereço de email principal será aceito. É uma propriedade em um contêiner de catálogo de endereços de contatos e uma coluna na tabela de contêineres do catálogo de endereços de contato.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

