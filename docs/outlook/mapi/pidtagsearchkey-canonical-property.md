---
title: Propriedade canônica PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595388"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propriedade canônica PidTagSearchKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma chave binário-comparável que identifica objetos correlatas para uma pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x300B  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de identificação  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade fornece um rastreamento para objetos relacionados, como cópias da mensagem e facilita a encontrar ocorrências indesejadas, como destinatários duplicados.
  
O MAPI usa regras específicas para a construção de chaves de pesquisa para os destinatários da mensagem. A chave de pesquisa é formada concatenando o tipo de endereço (em caracteres maiusculos), o caractere de dois-pontos ':', o endereço de email em forma canônica e o caractere de terminação null. Forma canônica aqui significa que diferencia maiusculas de minúsculas endereços aparecem em maiusculas e minúsculas, e os endereços que não diferenciam maiusculas de minúsculas são convertidos em maiusculos. Isso é importante na preservação correlações entre mensagens.
  
Para objetos de mensagem, essa propriedade está disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) imediatamente após a criação da mensagem. Para outros objetos, está disponível após a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Como essa propriedade é podem ser alterada, ele não é confiável obtê-lo por meio de **GetProps** até que uma chamada **SaveChanges** foi confirmada quaisquer valores definidos ou alterados pelo método [IMAPIProp::SetProps](imapiprop-setprops.md) . 
  
Para os perfis, MAPI também fornece uma seção de perfil codificadas denominada **MUID_PROFILE_INSTANCE**, com esta propriedade como sua propriedade única. Essa chave é garantido que ser exclusivo entre todos os perfis que nunca foi criados e pode ser mais confiável do que a propriedade **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que pode ser, por exemplo, excluída e recriada com o mesmo nome.
  
A tabela a seguir resume as diferenças importantes entre **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e essa propriedade.
  
|**Característica**|PR_ENTRYID * * *|PR_RECORD_KEY * * *|PR_SEARCH_KEY * * *|
|:-----|:-----|:-----|:-----|
|Necessários nos objetos attachment  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de pasta  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de repositório de mensagem  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de status  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|Creatable pelo cliente  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Disponíveis antes **SaveChanges** <br/> |Depende da implementação do provedor  <br/> |Depende da implementação do provedor  <br/> |Para mensagens, Sim. Para outras pessoas, ela depende da implementação do provedor.  <br/> |
|Alterado em uma operação de cópia  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Podem ser alterados pelo cliente após uma cópia  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Unique dentro …  <br/> |Mundo inteiro  <br/> |Instância do provedor  <br/> |Mundo inteiro  <br/> |
|Binário comparável (assim como acontece com memcmp)  <br/> |Não-- use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sim  <br/> |Sim  <br/> |
   
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



[Propriedade canônica PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propriedade canônica PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

