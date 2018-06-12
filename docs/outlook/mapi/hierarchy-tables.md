---
title: Tabelas de hierarquias
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 23314418836893b40cbddf3b90bd95ec061a00c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766713"
---
# <a name="hierarchy-tables"></a>Tabelas de hierarquias

  
  
**Aplica-se a**: Outlook 
  
Uma tabela de hierarquia contém informações sobre as pastas em um armazenamento de mensagens ou os contêineres em um contêiner de catálogo de endereços. Cada linha de uma tabela de hierarquia contém um conjunto de colunas com informações sobre uma pasta ou contêiner de catálogo de endereços. Tabelas de hierarquias principalmente são usadas pelos clientes e implementadas por provedores de armazenamento de mensagem para mostrar uma árvore de pastas e subpastas e implementadas pelos provedores de catálogo de endereços para mostrar uma árvore de contêineres no catálogo de endereços. Contêineres que não podem conter subcontêineres, conforme indicado pela ausência do sinalizador AB_SUBCONTAINERS em suas propriedades **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), não implementam uma tabela de hierarquia.
  
Uma tabela de hierarquia pode ser acessada chamando:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) passando **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) como a marca de propriedade e IID_IMAPITable como o identificador de interface.
    
Pastas e contêineres devem suportar ambas as técnicas para recuperar as propriedades de tabela. Ele é inaceitável para provedores de serviços oferecer suporte a apenas uma maneira de acessar nestas tabelas, pois clientes prevê que terá a opção. 
  
> [!IMPORTANT]
> Provedores de armazenamento não há uma garantia honram especificada para tabelas de hierarquias de definir a ordem de classificação. 
  
A chamada para **IMAPIProp::OpenProperty** envolve acessando a tabela de hierarquia abrindo sua propriedade correspondente, **PR_CONTAINER_HIERARCHY**. Embora **PR_CONTAINER_HIERARCHY** não podem ser recuperadas por meio de uma pasta ou o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner, ele é incluído na matriz de marca de propriedade que é retornado pelo método [IMAPIProp::GetPropList](imapiprop-getproplist.md) . 
  
 **PR_CONTAINER_HIERARCHY** também pode ser usado para incluir ou excluir uma tabela de hierarquia de uma operação de cópia. Se um cliente especifica **PR_CONTAINER_HIERARCHY** no parâmetro *lpExcludeProps* para [IMAPIProp::CopyTo](imapiprop-copyto.md) em uma operação de cópia, a nova pasta ou o contêiner não dará suporte a tabela de hierarquia da pasta original ou do contêiner. 
  
As seguintes propriedades formam o conjunto em uma tabela de hierarquia de colunas necessárias:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contém o nome para o contêiner ou a pasta que deve aparecer na exibição da hierarquia. 
  
 **PR_ENTRYID** é o identificador de entrada associado a este contêiner ou a pasta. Espera-se para ser um identificador de entrada de longo prazo. Clientes e MAPI podem passar esse identificador de entrada para **OpenEntry** para abrir o contêiner ou a pasta e acessar seu conteúdo chamando [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** é um valor numérico que indica o nível de recuo para este contêiner ou a pasta com zero sendo de nível superior. Mais aprofundado na hierarquia de um contêiner ou a pasta reside, quanto maior o valor de sua propriedade **PR_DEPTH** . Clientes usam a propriedade **PR_DEPTH** para exibir uma tabela de hierarquia apropriadamente, para que os usuários podem ver claramente relações pai/filho. Profundidade de contêiner ou a pasta é sempre em relação à contêiner ou implementando a tabela de hierarquia de pasta. 
  
 **PR_OBJECT_TYPE** sempre é definida como MAPI_ABCONT para tabelas de hierarquias de catálogo de endereços e MAPI_FOLDER para tabelas de hierarquias de pasta. 
  
 **PR_DISPLAY_TYPE** é um valor numérico que se refere à como um contêiner ou a pasta é exibida na tabela de hierarquia. Ele é usado principalmente para fins de exibição para diferenciar visualmente os tipos de contêineres ou pastas. Mensagem muitos armazenar e ícones de uso de provedores de livro para os tipos de exibição diferentes de endereços. É o provedor de fornecer esses ícones; MAPI não fornecer padrões. 
  
MAPI define os valores de muitos para **PR_DISPLAY_TYPE**, alguns que são válidos para outras pessoas que são usados com os índices de hierarquia de contêineres do catálogo de endereços e pastas. Normalmente, **PR_DISPLAY_TYPE uma pasta** é definida para DT_FOLDER para indicar um ícone de pasta padrão, DT_FOLDER_LINK para indicar um ícone que representa um link para outra pasta ou DT_FOLDER_SPECIAL para indicar um ícone que é específico do aplicativo. DT_FOLDER_LINK é usado com pastas de resultados de pesquisa. 
  
Além destas colunas obrigatórias, tabelas de hierarquias de catálogo de endereços devem incluir a propriedade **PR_CONTAINER_FLAGS** . **PR_CONTAINER_FLAGS** indica vários atributos sobre um contêiner na hierarquia e é usado para diferenciar o contêiner de um do outro. 
  
Uma propriedade opcional para tabelas de hierarquias de catálogo de endereços é a propriedade **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
Tabelas de hierarquias de armazenamento de mensagens incluem essas propriedades em seu conjunto de coluna necessária:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Provedores de catálogo de endereços devem suportar os seguintes métodos **IMAPITable** em suas implementações de tabela da hierarquia porque são necessárias para o catálogo de endereços integrada de MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable:: FindRow](imapitable-findrow.md) <br/> |[IMAPITable:: Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable:: QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

