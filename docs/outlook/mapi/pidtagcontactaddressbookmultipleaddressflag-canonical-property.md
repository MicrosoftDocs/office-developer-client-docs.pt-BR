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
ms.openlocfilehash: 42f164f09dbffcc05986771aa05f7ce14eee789c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769065"
---
# <a name="pidtagcontactaddressbookmultipleaddressflag-canonical-property"></a>Propriedade canônica PidTagContactAddressBookMultipleAddressFlag

  
  
**Aplica-se a**: Outlook 
  
Contém um sinalizador que será TRUE quando o provedor oferece suporte a vários endereços de email por item de contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONTAB_MULTI_ADDR_FLAG  <br/> |
|Identificador:  <br/> |0x6614  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Catálogo de endereços de contatos  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade for TRUE, o provedor não permite contatos sem endereços de email. Se for FALSE, o provedor mostra todos os contatos ou não terem um endereço de email primário. Somente o endereço de email primário será atendido. Esta é uma propriedade em um contêiner de catálogo de endereços de contatos e uma coluna na tabela de contêineres do catálogo de endereços de contatos.
  
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

