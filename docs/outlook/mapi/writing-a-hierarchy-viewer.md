---
title: Escrevendo um Visualizador de Hierarquias
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5f6ebd20afc3b8d029fa7c632c55982862664055
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421127"
---
# <a name="writing-a-hierarchy-viewer"></a>Escrevendo um Visualizador de Hierarquias

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador de hierarquias é um componente de interface do usuário usado para exibir tabelas de hierarquia de contêineres de pasta e de livro de endereços. Os visualizadores de hierarquia podem exibir membros da hierarquia em níveis diferentes, expandindo e contratando cada nível sob demanda.
  
A propriedade de contêiner, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla o nível no qual um membro da hierarquia é exibido. As entradas que representam contêineres ou pastas de lista de endereços de nível superior têm sua **PR_DEPTH** definida como zero. O valor dessa propriedade é incrementado sequencialmente para entradas em níveis sequenciais. Ou seja, quando um usuário seleciona um contêiner de nível superior para expandir, exibe todos os contêineres com PR_DEPTH **definido** como 1. Quando um usuário expande um desses subcontainers,  exibe os contêineres com PR_DEPTH definido como 2 e assim por diante. 
  
Visualizadores de hierarquia suportam uma variedade diferente de profundidades. Você pode limitar o visualizador a apenas um ou dois níveis ou pode dar suporte a vários níveis, se a exibição de uma hierarquia expansiva for uma prioridade. 
  
O livro de endereços fornece um visualizador de hierarquias para os contêineres de nível superior no livro de endereços. 
  
 **Para acessar a tabela de hierarquia do livro de endereços**
  
1. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando um identificador de entrada nulo, para abrir o contêiner raiz do livro de endereços.
    
2. Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) do contêiner raiz para acessar a tabela de hierarquia do livro de endereços MAPI. 
    
 **Para acessar a tabela de hierarquia do armazenamento de mensagens padrão**
  
1. Chame [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para acessar a tabela do armazenamento de mensagens. 
    
2. Crie uma **restrição** usando a estrutura [SPropertyRestriction](spropertyrestriction.md) para limitar a tabela apenas às linhas que tenham uma propriedade PR_DEFAULT_STORE ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) definida como TRUE. 
    
3. Chame [IMAPITable::FindRow](imapitable-findrow.md), passando o **SPropertyRestriction** para localizar a linha que representa o armazenamento de mensagens padrão. 
    
4. Chame [IMAPISession::OpenEntry](imapisession-openentry.md), passando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do armazenamento de mensagens padrão na tabela do armazenamento de mensagens.
    
5. Chame o método [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) .
    
6. Chame o método [IMsgStore::OpenEntry](imsgstore-openentry.md) do repositório de mensagens, passando a propriedade **PR_IPM_SUBTREE_ENTRYID,** para abrir a pasta raiz da subárvore IPM do repositório de mensagens. 
    
7. Chame o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) da pasta raiz do IPM para acessar sua tabela de hierarquia. 
    

