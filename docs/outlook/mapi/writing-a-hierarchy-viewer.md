---
title: Gravar um visualizador de hierarquia
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4c939a8c-8148-4add-b181-5a12e6d32309
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6ff394c95dfa3166d39dcba4b0c577dcfac7b8d8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581591"
---
# <a name="writing-a-hierarchy-viewer"></a>Gravar um visualizador de hierarquia

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador de hierarquia é um componente de interface do usuário que é usado para exibir a pasta e o endereço de tabelas de hierarquias de contêiner de catálogo. Visualizadores de hierarquia podem exibir os membros da hierarquia em níveis diferentes, expandindo e firmando contrato cada nível sob demanda.
  
A propriedade container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla o nível no qual um membro de hierarquia é exibido. Entradas que representam os contêineres do catálogo de endereços de nível superior ou pastas têm sua propriedade **PR_DEPTH** definida como zero. O valor dessa propriedade é incrementado sequencialmente para entradas nos níveis sequenciais. Ou seja, quando o usuário seleciona um contêiner de nível superior para expandir e exibir todos os contêineres com **PR_DEPTH** é definida como 1. Quando um usuário expande um desses subcontêineres, exibir os contêineres com **PR_DEPTH** definido como 2 e assim por diante. 
  
Visualizadores de hierarquia oferecem suporte a um intervalo diferente de Profundidades. Você pode limitar o visualizador a apenas um ou dois níveis, ou você pode oferecer suporte a vários níveis, se a exibição de uma hierarquia expansiva é uma prioridade. 
  
O catálogo de endereços fornece um visualizador de hierarquia para os recipientes de nível superior no catálogo de endereços. 
  
 **Para acessar a tabela de hierarquia de catálogo de endereços**
  
1. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md), passando um identificador de entrada nulo, para abrir o contêiner de raiz do catálogo de endereços.
    
2. Chame o método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) do contêiner raiz para acessar a tabela de hierarquia do catálogo de endereços MAPI. 
    
 **Para acessar a tabela de hierarquia do armazenamento de mensagens padrão**
  
1. Chame [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) para acessar a tabela de repositório de mensagens. 
    
2. Construa uma restrição usando a estrutura de [SPropertyRestriction](spropertyrestriction.md) para limitar a tabela de somente as linhas que possuem uma propriedade de **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) definida como TRUE. 
    
3. Chame [IMAPITable:: FindRow](imapitable-findrow.md), passando-lhe o **SPropertyRestriction**, para localizar a linha que representa o armazenamento de mensagens padrão. 
    
4. Chame [IMAPISession::OpenEntry](imapisession-openentry.md), passando na propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do armazenamento de mensagens padrão da tabela de repositório de mensagem.
    
5. Chame o método de [IMAPIProp::GetProps](imapiprop-getprops.md) do armazenamento de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Chame o método de [IMsgStore::OpenEntry](imsgstore-openentry.md) do armazenamento de mensagens, passando a propriedade **PR_IPM_SUBTREE_ENTRYID** , para abrir a pasta raiz do subárvore IPM do armazenamento de mensagens. 
    
7. Chame o método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) da pasta raiz IPM para acessar sua tabela de hierarquia. 
    

