---
title: Acessar os membros de uma lista de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a32552343fa90dfbbb3571f50846976a5f5f5edd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595360"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Acessar os membros de uma lista de distribuição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para obter os membros de uma lista de distribuição**
  
1. Criar uma matriz de marca de propriedade dimensionado com as propriedades dos membros que você deseja recuperar, como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir a lista de distribuição. 
    
3. Chame o método de **IABContainer::GetContentsTable** da lista de distribuição para acessar sua tabela de conteúdo. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas da tabela que representa os membros da lista de distribuição. 
    

