---
title: Acessando os membros de uma lista de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412384"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Acessando os membros de uma lista de distribuição

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para obter os membros de uma lista de distribuição**
  
1. Crie uma matriz de marca de propriedade dimensionada com as propriedades dos membros que você gostaria de recuperar, como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir a lista de distribuição. 
    
3. Chame o método **IABContainer::GetContentsTable** da lista de distribuição para acessar sua tabela de conteúdo. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas da tabela que representam os membros da lista de distribuição. 
    

