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
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328585"
---
# <a name="pidtagentryid-canonical-property"></a>Propriedade canônica PidTagEntryId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um identificador de entrada MAPI usado para abrir e editar propriedades de um objeto MAPI específico. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ENTRYID  <br/> |
|Identificador:  <br/> |0x0FFF  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de ID  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade identifica um objeto para **OpenEntry** in instantiate e fornece acesso a todas as suas propriedades por meio da interface derivada apropriada de **IMAPIProp**. 
  
Essa propriedade é uma das propriedades de endereço base para todos os usuários de mensagens. 
  
Essa propriedade pode conter um identificador de longo prazo ou de curto prazo. Identificadores de curto prazo são mais fáceis e rápidos de construir, mas são limitados em seu escopo e duração, normalmente para a sessão atual e estação de trabalho. Elas são comumente usadas para objetos de natureza temporária, como linhas de tabela ou entradas de caixa de diálogo, e então abandonadas. Identificadores de longo prazo são usados para objetos de uma natureza mais ampla e longa. 
  
Essa propriedade está sempre disponível por meio do método [IMAPIProp::GetProps](imapiprop-getprops.md) após a primeira chamada para o método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Alguns provedores de serviços podem torná-lo disponível imediatamente após a instaciação. O provedor deve sempre retornar um identificador de entrada de longo prazo de **GetProps**. Portanto, para converter um identificador de curto prazo em longo prazo, basta abrir o objeto e obter sua propriedade por meio **de GetProps**. 
  
A tabela a seguir resume diferenças importantes entre essa propriedade, **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Característica**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Obrigatório em objetos anexos  <br/> |Não  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório em objetos de pasta  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório nos objetos do armazenamento de mensagens  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Obrigatório em objetos de status  <br/> |Sim  <br/> |Não  <br/> |Não  <br/> |
|Criado pelo cliente  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Disponível antes da chamada para **SaveChanges** <br/> |Depende da implementação do provedor  <br/> |Depende da implementação do provedor  <br/> |Para mensagens, Sim. Para outros, depende da implementação do provedor.  <br/> |
|Alterado em uma operação de cópia  <br/> |Sim  <br/> |Sim  <br/> |Não  <br/> |
|Alterável pelo cliente após uma cópia  <br/> |Não  <br/> |Não  <br/> |Sim  <br/> |
|Exclusivo dentro  <br/> |Mundo inteiro  <br/> |Instância do provedor  <br/> |Mundo inteiro  <br/> |
|Binário comparável (como com memcmp)  <br/> |Não use [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sim  <br/> |Sim  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Lida com a recuperação de listas de permissões de pasta armazenadas no servidor.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Especifica métodos para conectar e configurar caixas de correio como representantes e interações com objetos de mensagem e calendário quando eles agem em nome de outro usuário.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Especifica o esquema e os métodos usados para solicitar informações de disponibilidade para usuários e recursos.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

