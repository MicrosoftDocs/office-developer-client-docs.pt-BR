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
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439678"
---
# <a name="required-features-for-address-book-containers"></a>Recursos necessários para contêineres do catálogo de endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A maioria dos provedores de catálogos de endereços oferece suporte a pelo menos um contêiner, alguns deles modificáveis. Os contêineres do catálogo de endereços podem fornecer conteúdo e tabelas de hierarquia, recursos de pesquisa e resolução de nomes. Os contêineres modificáveis permitem a exclusão de entradas, como usuários de mensagens, listas de distribuição ou outros contêineres e a adição de entradas de entradas em outros contêineres ou de modelos únicos.
  
A tabela a seguir descreve os recursos que são necessários para provedores de catálogo de endereços que possuem contêineres, modificáveis ou somente leitura e como você os implementa.
  
|**Recurso**|**Como implementar**|
|:-----|:-----|
|Usuários de mensagens de acesso  <br/> |Implemente o método [IABLogon:: OpenEntry](iablogon-openentry.md) . Para obter mais informações, consulte [abrir entradas do catálogo de endereços](opening-address-book-entries.md).  <br/> |
|Comparar usuários de mensagens  <br/> |Implemente o método [IABLogon:: CompareEntryIDs](iablogon-compareentryids.md) . Para obter mais informações, consulte comparando [entradas do catálogo de endereços](comparing-address-book-entries.md).  <br/> |
|Criar usuários de mensagens  <br/> |1. forneça uma lista de modelos de criação em uma tabela única, com suporte para a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Para obter mais informações, consulte [Implementing a container one-off Table](implementing-a-container-one-off-table.md).  <br/> 2. implemente o método [IABContainer:: createentry](iabcontainer-createentry.md) . Para obter mais informações, consulte [adicionando entradas do catálogo de endereços](adding-address-book-entries.md).  <br/> |
|Copiar usuários de mensagens  <br/> |Implemente o método [IABContainer:: CopyEntries](iabcontainer-copyentries.md) . Para obter mais informações, consulte [copiaNdo entradas do catálogo de endereços](copying-address-book-entries.md).  <br/> |
|Remover usuários de mensagens  <br/> |Implemente o método [IABContainer::D eleteentries](iabcontainer-deleteentries.md) . Para obter mais informações, consulte [removeNdo entradas do catálogo de endereços](removing-address-book-entries.md).  <br/> |
|Fornecer informações de resumo sobre usuários de mensagens  <br/> |Suporta a propriedade container **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Para mais informações, confira [Tabelas de Conteúdo](contents-tables.md).  <br/> |
|Fornecer informações detalhadas sobre usuários de mensagens  <br/> |Suporta a propriedade **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em usuários de mensagens e listas de distribuição. Para obter mais informações, consulte [exibiNdo informações do destinatário](displaying-recipient-information.md) e [Exibir tabelas](display-tables.md).  <br/> |
|Fornecer informações detalhadas sobre um contêiner  <br/> |Oferecer suporte à propriedade **PR_DETAILS_TABLE** no contêiner. Para obter mais informações, consulte [exibiNdo informações do destinatário](displaying-recipient-information.md) e [Exibir tabelas](display-tables.md).  <br/> |
|Fornecer uma lista hierárquica de contêineres  <br/> |Suporta a propriedade container **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Para obter mais informações, consulte [tabelas de hierarquia](hierarchy-tables.md).  <br/> |
|Suporte a propriedades de usuários de mensagens  <br/> |Implemente a interface [IMailUser: IMAPIProp](imailuserimapiprop.md)  <br/> |
|Resolver nomes ambíguos  <br/> | Suporta a restrição de propriedade **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  Opcionalmente, implemente o método [IABContainer:: ResolveNames](iabcontainer-resolvenames.md) . Para obter mais informações, consulte [implementaNdo resolução de nomes](implementing-name-resolution.md).  <br/> |
   

