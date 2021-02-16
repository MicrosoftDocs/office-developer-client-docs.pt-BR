---
title: Propriedade canônica PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342534"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Propriedade canônica PidTagMappingSignature

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a assinatura de mapeamento para propriedades nomeadas de um objeto MAPI específico. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Identificador:  <br/> |0x0FF8  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que objetos com propriedades nomeadas exponham essa propriedade. Um aplicativo cliente deve verificar **PR_MAPPING_SIGNATURE** propriedade de ambos os objetos ao copiar propriedades nomeadas de um objeto para outro. O uso dessa propriedade pode minimizar a tradução entre os nomes e identificadores das propriedades copiadas. 
  
Se essa propriedade não existir para um determinado objeto MAPI, o objeto terá seu próprio mapeamento exclusivo de nomes e identificadores. Nesse caso, o cliente deve chamar o método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) no objeto de origem e, em seguida, o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) no objeto de destino. 
  
Quando dois objetos têm o mesmo **PR_MAPPING_SIGNATURE,** o cliente não precisa traduzir o nome para identificador e identificador para o nome. O cliente pode simplesmente chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) na origem e, em seguida, o método [IMAPIProp::SetProps](imapiprop-setprops.md) no destino. Isso é conveniente para clientes que realizam cópia personalizada de propriedades nomeadas e para provedores implementando os métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps.](imapiprop-copyprops.md) 
  
Para obter mais informações sobre propriedades nomeadas e mapeamento de nomes e identificadores, consulte [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[MAPINAMEID](mapinameid.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

