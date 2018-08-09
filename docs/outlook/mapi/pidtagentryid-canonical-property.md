---
title: Propriedade canônica PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769236"
---
# <a name="pidtagentryid-canonical-property"></a>Propriedade canônica PidTagEntryId

  
  
**Aplica-se a**: Outlook 
  
Contém um identificador de entrada MAPI usado para abrir e editar as propriedades de um determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de identificação  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade identifica um objeto para **OpenEntry** instanciar e fornece acesso a todas as suas propriedades por meio da interface derivada apropriada de **IMAPIProp**. 
  
Essa propriedade é uma das propriedades endereço base para todos os usuários de mensagens. 
  
Essa propriedade pode conter um longo prazo ou um identificador de curto prazo. Identificadores de curto prazo são mais fácil e rápido para construção, mas estão limitados em seu escopo e a duração, geralmente para a sessão atual e a estação de trabalho. Elas são usadas para objetos de natureza temporária, como linhas da tabela ou entradas da caixa de diálogo e então abandonadas. Identificadores de longo prazo são usados para objetos de natureza mais ampla e de longa duração. 
  
Essa propriedade sempre está disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada ao método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Alguns provedores de serviços podem disponibilizá-lo imediatamente após instanciação. O provedor sempre deve retornar um identificador de entrada de longo prazo do **GetProps**. Portanto, para converter um identificador curto prazo longo prazo, simplesmente abre o objeto e obter seu essa propriedade por meio de **GetProps**. 
  
A tabela a seguir resume as diferenças importantes entre essa propriedade, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Necessários nos objetos attachment  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de pasta  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de repositório de mensagem  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Necessários nos objetos de status  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|Criado pelo cliente  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Disponíveis antes da chamada para **SaveChanges** <br/> |Depende da implementação do provedor  <br/> |Depende da implementação do provedor  <br/> |Para mensagens, Sim. Para outras pessoas, depende da implementação do provedor.  <br/> |
|Alterado em uma operação de cópia  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Podem ser alterados pelo cliente após uma cópia  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Exclusiva dentro  <br/> |Mundo inteiro  <br/> |Instância do provedor  <br/> |Mundo inteiro  <br/> |
|Binário comparável (assim como acontece com memcmp)  <br/> |Sem uso [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sim  <br/> |Sim  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Trata a recuperação de listas de permissão de pastas que são armazenados no servidor.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica os métodos para conexão e a configuração de caixas de correio conforme representantes e as interações com objetos de mensagem e o calendário quando eles ajam em nome de outro usuário.
    
[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Especifica o esquema e métodos que são usados para solicitar informações de disponibilidade para usuários e recursos.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

