---
title: Criar um visualizador de hierarquia
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
# <a name="writing-a-hierarchy-viewer"></a>Criar um visualizador de hierarquia

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador de hierarquia é um componente de interface de usuário usado para exibir as tabelas de hierarquia de contêiner de pasta e catálogo de endereços. Os visualizadores de hierarquia podem exibir membros da hierarquia em diferentes níveis, expandindo e contratando cada nível sob demanda.
  
A propriedade container, **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)), controla o nível no qual um membro de hierarquia é exibido. As entradas que representam recipientes ou pastas de catálogo de endereços de nível superior têm a propriedade **PR_DEPTH** definida como zero. O valor dessa propriedade é incrementalmente em sequência para entradas em níveis sequenciais. Ou seja, quando um usuário seleciona um contêiner de nível superior para expandir, exiba todos os contêineres com **PR_DEPTH** definido como 1. Quando um usuário expande um desses sub-recipientes, exibe os contêineres com **PR_DEPTH** definido como 2 e assim por diante. 
  
Os visualizadores de hierarquia dão suporte a um intervalo diferente de profundidades. Você pode limitar o seu visualizador a apenas um ou dois níveis, ou pode dar suporte a vários níveis, se a exibição de uma hierarquia de baixo for uma prioridade. 
  
O catálogo de endereços fornece um visualizador de hierarquia para os recipientes de nível superior no catálogo de endereços. 
  
 **Para acessar a tabela de hierarquia de catálogo de endereços**
  
1. Chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md), passando um identificador de entrada nulo, para abrir o contêiner raiz do catálogo de endereços.
    
2. Chame o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable do contêiner raiz para acessar a tabela de hierarquia do catálogo de endereços MAPI. 
    
 **Para acessar a tabela de hierarquia do repositório de mensagens padrão**
  
1. Chame [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) para acessar a tabela do repositório de mensagens. 
    
2. Crie uma restrição usando a estrutura [SPropertyRestriction](spropertyrestriction.md) para limitar a tabela apenas às linhas que têm uma propriedade **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) definida como true. 
    
3. Call [IMAPITable:: FindRow](imapitable-findrow.md), passando-o **SPropertyRestriction**para localizar a linha que representa o repositório de mensagens padrão. 
    
4. Chame [IMAPISession:: OpenEntry](imapisession-openentry.md), passando a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do repositório de mensagens padrão na tabela do repositório de mensagens.
    
5. Chame o método [IMAPIProp::](imapiprop-getprops.md) GetProps do repositório de mensagens para recuperar a propriedade **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)).
    
6. Chame o método [IMsgStore:: OpenEntry](imsgstore-openentry.md) do repositório de mensagens, passando a propriedade **PR_IPM_SUBTREE_ENTRYID** , para abrir a pasta raiz da sub-árvore IPM do repositório de mensagens. 
    
7. Chame o método [IMAPIContainer::](imapicontainer-gethierarchytable.md) GetHierarchyTable da pasta raiz IPM para acessar sua tabela de hierarquia. 
    

