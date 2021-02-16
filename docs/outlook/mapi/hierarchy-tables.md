---
title: Tabelas de Hierarquias
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8aa6b36-d6e5-4e1f-8ac5-5d6a78a70bf8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2a1461f0c7196cd425d9736f5837b742bedd4fb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428365"
---
# <a name="hierarchy-tables"></a>Tabelas de Hierarquias

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de hierarquia contém informações sobre as pastas em um armazenamento de mensagens ou os contêineres em um contêiner de um livro de endereços. Cada linha de uma tabela de hierarquia contém um conjunto de colunas com informações sobre uma pasta ou contêiner de agenda de endereços. As tabelas de hierarquias são usadas principalmente por clientes e implementadas por provedores de armazenamento de mensagens para mostrar uma árvore de pastas e subpastas e implementadas por provedores de agendas para mostrar uma árvore de contêineres no livro de endereços. Contêineres que não podem manter subcontainers, conforme indicado pela ausência do sinalizador AB_SUBCONTAINERS em sua propriedade **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)), não implementam uma tabela de hierarquia.
  
Uma tabela de hierarquia pode ser acessada chamando:
  
- [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).
    
    - Ou -
    
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md) passando **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) como a marca de propriedade e IID_IMAPITable como o identificador da interface.
    
Contêineres e pastas devem dar suporte a ambas as técnicas para recuperar as propriedades da tabela. É inaceitável para os provedores de serviços dar suporte apenas a uma maneira de acessar essas tabelas, pois os clientes esperam ter a opção. 
  
> [!IMPORTANT]
> Não há garantia de que os provedores da loja adquiram o conjunto de ordem de classificação especificado para tabelas de hierarquia. 
  
A chamada para **IMAPIProp::OpenProperty** envolve acessar a tabela de hierarquia abrindo sua propriedade correspondente, **PR_CONTAINER_HIERARCHY**. Embora **PR_CONTAINER_HIERARCHY** não possa ser recuperado por meio de uma pasta ou do método [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner, ele é incluído na matriz de marca de propriedade que é retornada pelo método [IMAPIProp::GetPropList.](imapiprop-getproplist.md) 
  
 **PR_CONTAINER_HIERARCHY** também pode ser usado para incluir ou excluir uma tabela de hierarquia de uma operação de cópia. Se um cliente especificar PR_CONTAINER_HIERARCHY no parâmetro *lpExcludeProps* para [IMAPIProp::CopyTo](imapiprop-copyto.md) em uma operação de cópia, a nova pasta ou contêiner não dará suporte **à** tabela de hierarquia da pasta ou contêiner original. 
  
As propriedades a seguir compom o conjunto de colunas necessário em uma tabela de hierarquia:
  
|||
|:-----|:-----|
|**PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md))  <br/> |**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md))  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_STATUS** ([PidTagStatus](pidtagstatus-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** contém o nome do contêiner ou pasta que deve aparecer na exibição da hierarquia. 
  
 **PR_ENTRYID** é o identificador de entrada associado a esse contêiner ou pasta. Espera-se que seja um identificador de entrada de longo prazo. Clientes e MAPI podem passar esse identificador de entrada para **OpenEntry** para abrir o contêiner ou pasta e exibir seu conteúdo chamando [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). 
  
 **PR_DEPTH** é um valor numérico que indica o nível de recuo para esse contêiner ou pasta com zero sendo o nível superior. Quanto mais profunda for a hierarquia em que um contêiner ou pasta reside, maior será o valor de sua **PR_DEPTH** propriedade. Os clientes usam **a PR_DEPTH** para exibir uma tabela de hierarquia adequadamente, para que os usuários possam ver claramente as relações pai e filho. A profundidade do contêiner ou pasta é sempre relativa ao contêiner ou pasta que implementa a tabela de hierarquias. 
  
 **PR_OBJECT_TYPE** é sempre definido como MAPI_ABCONT para tabelas de hierarquias de pastas de endereços e MAPI_FOLDER tabelas de hierarquia de pastas. 
  
 **PR_DISPLAY_TYPE** é um valor numérico relacionado a como um contêiner ou pasta é exibido na tabela de hierarquia. Ele é usado principalmente para fins de exibição, para diferenciar visualmente entre tipos de contêineres ou pastas. Muitos provedores de armazenamento de mensagens e de address book usam ícones para os diferentes tipos de exibição. O provedor deve fornecer esses ícones; MAPI does not supply defaults. 
  
MAPI define muitos valores para **PR_DISPLAY_TYPE**, alguns que são válidos para pastas e outros que são usados com as tabelas de hierarquia de contêineres de livro de endereços. Normalmente, o PR_DISPLAY_TYPE  de uma pasta é definido como DT_FOLDER para indicar um ícone de pasta padrão, DT_FOLDER_LINK para indicar um ícone que representa um link para outra pasta ou DT_FOLDER_SPECIAL para indicar um ícone específico do aplicativo. DT_FOLDER_LINK é usado com pastas de resultados de pesquisa. 
  
Além dessas colunas necessárias, as tabelas de hierarquia do livro de endereços devem incluir PR_CONTAINER_FLAGS **propriedade.** **PR_CONTAINER_FLAGS** indica vários atributos sobre um contêiner na hierarquia e é usado para distinguir um contêiner de outro. 
  
Uma propriedade opcional para tabelas de hierarquia do livro de endereços é a **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)).
  
As tabelas de hierarquia do armazenamento de mensagens incluem essas propriedades no conjunto de colunas necessário:
  
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CONTENT_UNREAD** ([PidTagContentUnreadCount](pidtagcontentunreadcount-canonical-property.md))
    
Os provedores de lista de endereços devem dar suporte aos seguintes métodos **IMAPITable** em suas implementações de tabela de hierarquia, pois são exigidos pelo agendador de endereços integrado MAPI: 
  
|||
|:-----|:-----|
|[IMAPITable::QueryColumns](imapitable-querycolumns.md) <br/> |[IMAPITable::QueryPosition](imapitable-queryposition.md) <br/> |
|[IMAPITable::SeekRow](imapitable-seekrow.md) <br/> |[IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) <br/> |
|[IMAPITable::ExpandRow](imapitable-findrow.md) <br/> |[IMAPITable::Restrict](imapitable-restrict.md) <br/> |
|[IMAPITable::CreateBookmark](imapitable-createbookmark.md) <br/> |[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
|[IMAPITable::QueryRows](imapitable-queryrows.md) <br/> | <br/> |
   
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

