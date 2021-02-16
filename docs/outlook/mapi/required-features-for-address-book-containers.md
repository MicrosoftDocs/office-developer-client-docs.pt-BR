---
title: Recursos necessários para contêineres do Livro de Endereços
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
# <a name="required-features-for-address-book-containers"></a>Recursos necessários para contêineres do Livro de Endereços

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A maioria dos provedores de agendas de endereços suporta pelo menos um contêiner, alguns deles modificáveis. Os contêineres de agenda podem fornecer conteúdo e tabelas de hierarquia, recursos de pesquisa e resolução de nomes. Contêineres modificáveis permitem a exclusão de entradas como usuários de mensagens, listas de distribuição ou outros contêineres e a adição de entradas de entradas em outros contêineres ou de modelos one-off.
  
A tabela a seguir descreve os recursos necessários dos provedores de agendas que têm contêineres, modificáveis ou somente leitura e como implementá-los.
  
|**Característica**|**Como implementar**|
|:-----|:-----|
|Acessar usuários de mensagens  <br/> |Implemente [o método IABLogon::OpenEntry.](iablogon-openentry.md) Para obter mais informações, consulte [Abrindo entradas do Livro de Endereços.](opening-address-book-entries.md)  <br/> |
|Comparar usuários de mensagens  <br/> |Implemente [o método IABLogon::CompareEntryIDs.](iablogon-compareentryids.md) Para obter mais informações, consulte [Comparando entradas do Livro de Endereços.](comparing-address-book-entries.md)  <br/> |
|Criar usuários de mensagens  <br/> |1. Forneça uma lista de modelos de criação em uma tabela única, dando suporte à PR_CREATE_TEMPLATES **(** [PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Para obter mais informações, [consulte Implementando uma tabela de One-Off contêiner.](implementing-a-container-one-off-table.md)  <br/> 2. Implemente o [método IABContainer::CreateEntry.](iabcontainer-createentry.md) Para obter mais informações, consulte [Adicionando entradas do Livro de Endereços.](adding-address-book-entries.md)  <br/> |
|Copiar usuários de mensagens  <br/> |Implemente [o método IABContainer::CopyEntries.](iabcontainer-copyentries.md) Para obter mais informações, consulte [Copying Address Book Entries](copying-address-book-entries.md).  <br/> |
|Remover usuários de mensagens  <br/> |Implemente [o método IABContainer::D eleteEntries.](iabcontainer-deleteentries.md) Para obter mais informações, consulte [Removendo entradas do Livro de Endereços.](removing-address-book-entries.md)  <br/> |
|Fornecer informações resumidas sobre usuários de mensagens  <br/> |Suporte à propriedade de **contêiner PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Para mais informações, confira [Tabelas de Conteúdo](contents-tables.md).  <br/> |
|Fornecer informações detalhadas sobre usuários de mensagens  <br/> |Suporte à **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) em usuários de mensagens e listas de distribuição. Para obter mais informações, consulte [Exibindo informações do destinatário e](displaying-recipient-information.md) exibir [tabelas.](display-tables.md)  <br/> |
|Fornecer informações detalhadas sobre um contêiner  <br/> |Suporte a **PR_DETAILS_TABLE** propriedade no contêiner. Para obter mais informações, consulte [Exibindo informações do destinatário e](displaying-recipient-information.md) exibir [tabelas.](display-tables.md)  <br/> |
|Fornecer uma lista hierárquica de contêineres  <br/> |Suporte à propriedade de **contêiner PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Para obter mais informações, consulte [Tabelas de Hierarquia.](hierarchy-tables.md)  <br/> |
|Suporte a propriedades do usuário de mensagens  <br/> |Implemente [a interface IMailUser : IMAPIProp.](imailuserimapiprop.md)  <br/> |
|Resolver nomes ambíguos  <br/> | Suporte à **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) restrição de propriedade.  <br/>  Opcionalmente, implemente [o método IABContainer::ResolveNames.](iabcontainer-resolvenames.md) Para obter mais informações, consulte [Implementando a resolução de nomes.](implementing-name-resolution.md)  <br/> |
   

