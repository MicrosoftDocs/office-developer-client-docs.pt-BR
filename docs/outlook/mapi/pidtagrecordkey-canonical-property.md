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
ms.openlocfilehash: 7a3ae7db1fb97e97f7d0939b67f139af62477bf7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355262"
---
# <a name="pidtagrecordkey-canonical-property"></a>Propriedade canônica PidTagRecordKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador binário exclusivo comparável para um objeto específico.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECORD_KEY  <br/> |
|Identificador:  <br/> |0x0FF9  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de ID  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade facilita a localização de referências a um objeto, como localizar sua linha em uma tabela de conteúdo. Essa propriedade não pode ser usada para abrir um objeto; use o identificador de entrada para essa finalidade.
  
Um subobjeto de anexo deve ser identificado exclusivamente dentro de uma mensagem por essa propriedade. Esse identificador é a única característica de anexo garantida que se manterá a mesma depois que a mensagem for fechada e reaberta. O provedor de armazenamento deve preservar essa propriedade entre sessões para garantir essa garantia.
  
Para pastas, essa propriedade contém uma chave usada na tabela de hierarquia de pastas. Normalmente, esse é o mesmo valor fornecido pela propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
  
Para repositórios de mensagens, essa propriedade é idêntica à **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) .
  
Em um objeto de armazenamento de mensagens, essa propriedade deve ser exclusiva em todos os provedores de armazenamento. Uma maneira de fazer isso é combinar o valor da propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para o repositório (exclusivo para esse tipo de provedor) com uma estrutura [GUID](guid.md) ou outro valor exclusivo para o repositório de mensagens específico. 
  
Essa propriedade está sempre disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada para o método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Alguns provedores podem torná-lo disponível imediatamente após a instaciação. 
  
Um cliente ou provedor de serviços pode comparar valores dessa propriedade usando o memcmp. Isso não é possível para valores de identificador de entrada. No entanto, essa propriedade é garantida como exclusiva dentro do mesmo armazenamento de mensagens ou contêiner do livro de endereços; dois objetos de contêineres diferentes podem ter o mesmo valor dessa propriedade.
  
Uma distinção entre o registro e as teclas de pesquisa é que a chave de registro é específica para o objeto, enquanto a chave de pesquisa pode ser copiada para outros objetos. Por exemplo, duas cópias do objeto podem ter o mesmo **valor PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)), mas devem ter valores diferentes para essa propriedade.
  
A tabela a seguir resume diferenças importantes **entre PR_ENTRYID**, **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e esta propriedade. 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obrigatório em objetos anexos  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório em objetos de pasta  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório nos objetos do armazenamento de mensagens  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório em objetos de status  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|Criatável pelo cliente  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Disponível antes de uma chamada para **SaveChanges** <br/> |Talvez  <br/> |Talvez  <br/> |Mensagens Sim, Outras Talvez  <br/> |
|Alterado em uma operação de cópia  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Alterável por um cliente após uma cópia  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Exclusivo em ...  <br/> |Mundo inteiro  <br/> |Instância do provedor  <br/> |Mundo inteiro  <br/> |
|Binário comparável (como com memcmp)  <br/> |Não -- use **IMAPISupport:: CompareEntryIDs** <br/> |Sim  <br/> |Sim  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

