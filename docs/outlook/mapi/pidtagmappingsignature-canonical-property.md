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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396222"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Propriedade canônica PidTagMappingSignature

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a assinatura de mapeamento para propriedades nomeadas de um determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Identificador:  <br/> |0x0FF8  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Diversos  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os objetos tendo propriedades nomeadas exponham essa propriedade. Um aplicativo cliente deve verificar a propriedade **PR_MAPPING_SIGNATURE** dos dois objetos quando copiando nomeada propriedades de um objeto para outro. O uso dessa propriedade pode minimizar a conversão entre nomes e os identificadores de propriedades copiadas. 
  
Se essa propriedade não existe para um determinado objeto MAPI, o objeto tem seu próprio mapeamento exclusivo de nomes e os identificadores. Neste caso o cliente deve chamar o método de [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) no objeto de origem e, em seguida, o método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) no objeto de destino. 
  
Quando dois objetos têm o mesmo valor **PR_MAPPING_SIGNATURE** , o cliente não precisará traduzir o nome para o identificador e identificador de nome. O cliente pode simplesmente chamar o método [IMAPIProp::GetProps](imapiprop-getprops.md) na origem e, em seguida, o método [IMAPIProp::SetProps](imapiprop-setprops.md) no destino. Isso é conveniente para clientes que executam copiando personalizado propriedades nomeadas e para provedores Implementando os métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md) . 
  
Para obter mais informações sobre propriedades nomeadas e mapeamento de nomes e os identificadores, consulte [Propriedades de chamada de MAPI](mapi-named-properties.md). 
  
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
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[MAPINAMEID](mapinameid.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

