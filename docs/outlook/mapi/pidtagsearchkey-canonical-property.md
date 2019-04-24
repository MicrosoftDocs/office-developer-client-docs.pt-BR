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
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345462"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propriedade canônica PidTagSearchKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma chave comparável à binária que identifica objetos correlacionados para uma pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x300B  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de ID  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade fornece um rastreamento para objetos relacionados, como cópias de mensagens, e facilita a localização de ocorrências indesejadas, como destinatários duplicados.
  
O MAPI usa regras específicas para construir chaves de pesquisa para destinatários de mensagens. A chave de pesquisa é formada com a concatenação do tipo de endereço (em caracteres maiúsculos), o caractere de dois pontos ': ', o endereço de email em forma canônica e o caractere nulo de terminação. Forma canônica aqui significa que os endereços diferenciados entre maiúsculas e minúsculas aparecem no caso correto, e os endereços que não diferenciam maiúsculas de minúsculas são convertidos em maiúsculas. Isso é importante em preservar as correlações entre as mensagens.
  
Para objetos de mensagem, essa propriedade está disponível por meio do método [IMAPIProp::](imapiprop-getprops.md) GetProps imediatamente após a criação da mensagem. Para outros objetos, ele está disponível seguindo a primeira chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Como essa propriedade pode ser alterada, não é possível obtê-la por **** meio de GetProps até que uma chamada **SaveChanges** tenha confirmado quaisquer valores definidos ou alterados pelo método [IMAPIProp::](imapiprop-setprops.md) SetProps. 
  
Para perfis, o MAPI também fornece uma seção de perfil embutida com o nome **MUID_PROFILE_INSTANCE**, com essa propriedade como sua única propriedade. É garantido que essa chave seja exclusiva entre todos os perfis já criados e pode ser mais confiável do que a propriedade **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que pode ser, por exemplo, excluída e recriada com o mesmo nome.
  
A tabela a seguir resume diferenças importantes entre o **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), o **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e essa propriedade.
  
|**Características**|PR_ENTRYID * * * *|PR_RECORD_KEY * * * *|PR_SEARCH_KEY * * * *|
|:-----|:-----|:-----|:-----|
|Obrigatório em objetos Attachment  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório em objetos Folder  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório nos objetos do repositório de mensagens  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório nos objetos status  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|Criada por cliente  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Disponível antes de **SaveChanges** <br/> |Depende da implementação do provedor  <br/> |Depende da implementação do provedor  <br/> |Para mensagens, sim. Para outros, ele depende da implementação do provedor.  <br/> |
|Alterado em uma operação de cópia  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|É possível alterar o cliente após uma cópia  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Exclusivo em...  <br/> |Todo o mundo  <br/> |Instância do provedor  <br/> |Todo o mundo  <br/> |
|Binary comparável (como em memcmp)  <br/> |Não--use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sim  <br/> |Sim  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações de listas de usuários, contatos, grupos e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propriedade canônica PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

