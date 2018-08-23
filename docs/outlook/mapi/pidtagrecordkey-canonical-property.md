---
title: Propriedade canônica PidTagRecordKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecordKey
api_type:
- COM
ms.assetid: a12fb9a2-799d-4112-b26c-4b2854c47cc2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9add9246cdfb22f7c5ad579f425932f49d4a9ecd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581241"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propriedade canônica PidTagRecordKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador binário-comparável exclusivo para um objeto específico.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECORD_KEY  <br/> |
|Identificador:  <br/> |0x0FF9  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de identificação  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade facilita a localização referências a um objeto, como a localização de sua linha em uma tabela de conteúdo. Essa propriedade não pode ser usada para abrir um objeto; Use o identificador de entrada para essa finalidade.
  
Um Subobjeto anexo deve ser identificado exclusivamente dentro de uma mensagem por esta propriedade. Esse identificador é a única característica de anexo garantida que permanecem o mesmo depois que a mensagem é fechada e reabri-lo. O provedor de armazenamento deve preservar essa propriedade nas sessões para garantir que essa garantia.
  
Para pastas, essa propriedade contém uma chave usada na tabela de hierarquia de pasta. Normalmente, isso é o mesmo valor que é fornecida pela propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Para repositórios de mensagem, essa propriedade é idêntica à propriedade **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)).
  
Em um objeto de repositório de mensagem, esta propriedade deve ser exclusiva entre todos os provedores de armazenamento. Uma maneira de fazer isso é combinar o valor da propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para o repositório (exclusivo desse tipo de provedor) com uma estrutura [GUID](guid.md) ou outro valor exclusivo para o armazenamento de mensagem específica. 
  
Essa propriedade sempre está disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Alguns provedores podem disponibilizá-lo imediatamente após instanciação. 
  
Um provedor de cliente ou serviço pode comparar valores dessa propriedade usando memcmp. Isso não é possível para os valores de identificador de entrada. No entanto, essa propriedade é garantida ser exclusivo dentro do mesmo repositório de mensagem ou recipiente; do catálogo de endereços dois objetos dos contêineres diferentes podem ter o mesmo valor dessa propriedade.
  
Uma distinção entre as chaves de registro e de pesquisa é que a chave do registro é específica para o objeto, enquanto a chave de pesquisa pode ser copiada para outros objetos. Por exemplo, duas cópias do objeto podem ter o mesmo valor de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mas devem ter valores diferentes para esta propriedade.
  
A tabela a seguir resume as diferenças importantes entre **PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e essa propriedade. 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Necessários nos objetos attachment  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de pasta  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de repositório de mensagem  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de status  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|Creatable pelo cliente  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Disponíveis antes de uma chamada para **SaveChanges** <br/> |Talvez  <br/> |Talvez  <br/> |Mensagens de outras pessoas Sim talvez  <br/> |
|Alterado em uma operação de cópia  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Podem ser alterados por um cliente após uma cópia  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Unique dentro …  <br/> |Mundo inteiro  <br/> |Instância do provedor  <br/> |Mundo inteiro  <br/> |
|Binário comparável (assim como acontece com memcmp)  <br/> |Não-- use **IMAPISupport:: CompareEntryIDs** <br/> |Sim  <br/> |Sim  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

