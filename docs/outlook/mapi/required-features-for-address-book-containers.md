---
title: Recursos necessários para contêineres do catálogo de endereços
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5eeaa9a8c1965954ad2eb0a6bfd2a174a355f10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770259"
---
# <a name="required-features-for-address-book-containers"></a>Recursos necessários para contêineres do catálogo de endereços

  
  
**Aplica-se a**: Outlook 
  
A maioria dos provedores de catálogo de endereços oferecem suporte a pelo menos um contêiner, alguns deles pode ser modificado. Contêineres de catálogo de endereços podem fornecer conteúdo e tabelas de hierarquias, recursos de pesquisa e resolução de nomes. Contêineres modificáveis permitem a exclusão de entradas como mensagens de usuários, listas de distribuição, ou outros contêineres e a adição de entradas a partir de entradas em outros contêineres ou modelos únicos.
  
A tabela a seguir descreve os recursos necessários de provedores de catálogo de endereços que tenham contêineres, modificáveis ou somente leitura, e como implementá-las.
  
|**Recurso**|**Como implementar**|
|:-----|:-----|
|Usuários de mensagens do Access  <br/> |Implemente o método [IABLogon::OpenEntry](iablogon-openentry.md) . Para obter mais informações, consulte [Abertura entradas do catálogo de endereços](opening-address-book-entries.md).  <br/> |
|Comparar mensagens de usuários  <br/> |Implemente o método [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) . Para obter mais informações, consulte [Comparando entradas do catálogo de endereços](comparing-address-book-entries.md).  <br/> |
|Criar usuários de mensagens  <br/> |1. fornece uma lista de modelos de criação de uma tabela único, oferecendo suporte a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Para obter mais informações, consulte [Implementando uma tabela únicos do contêiner](implementing-a-container-one-off-table.md).  <br/> 2. implemente o método [IABContainer::CreateEntry](iabcontainer-createentry.md) . Para obter mais informações, consulte [Adicionar entradas do catálogo de endereços](adding-address-book-entries.md).  <br/> |
|Copiar mensagens de usuários  <br/> |Implemente o método [IABContainer::CopyEntries](iabcontainer-copyentries.md) . Para obter mais informações, consulte [Copiando entradas do catálogo de endereços](copying-address-book-entries.md).  <br/> |
|Remover mensagens de usuários  <br/> |Implemente o método [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) . Para obter mais informações, consulte [Removendo entradas do catálogo de endereços](removing-address-book-entries.md).  <br/> |
|Forneça as informações de resumo sobre as mensagens de usuários  <br/> |Suporte à propriedade **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) do contêiner. Para obter mais informações, consulte [As tabelas de conteúdo](contents-tables.md).  <br/> |
|Fornecer informações detalhadas sobre os usuários de mensagens  <br/> |Suporte à propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em usuários e listas de distribuição de mensagens. Para obter mais informações, consulte [Exibindo informações de destinatário](displaying-recipient-information.md) e [Tabelas de exibição](display-tables.md).  <br/> |
|Fornecer informações detalhadas sobre um contêiner  <br/> |Suporte à propriedade **PR_DETAILS_TABLE** no contêiner. Para obter mais informações, consulte [Exibindo informações de destinatário](displaying-recipient-information.md) e [Tabelas de exibição](display-tables.md).  <br/> |
|Fornecer uma lista hierárquica dos contêineres  <br/> |Suporte à propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) do contêiner. Para obter mais informações, consulte as [Tabelas de hierarquias](hierarchy-tables.md).  <br/> |
|Suporte a mensagens propriedades de usuário  <br/> |Implementar o [IMailUser: IMAPIProp](imailuserimapiprop.md) interface.  <br/> |
|Resolver nomes ambíguos  <br/> | Suporte a restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Opcionalmente, implemente o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . Para obter mais informações, consulte [Implementando a resolução de nome](implementing-name-resolution.md).  <br/> |
   

