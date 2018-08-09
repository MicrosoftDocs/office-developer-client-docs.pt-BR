---
title: Acessar os membros de uma lista de distribuição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766127"
---
# <a name="accessing-the-members-of-a-distribution-list"></a>Acessar os membros de uma lista de distribuição

  
  
**Aplica-se a**: Outlook 
  
 **Para obter os membros de uma lista de distribuição**
  
1. Criar uma matriz de marca de propriedade dimensionado com as propriedades dos membros que você deseja recuperar, como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) e **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
    
2. Chame [IAddrBook::OpenEntry](iaddrbook-openentry.md) para abrir a lista de distribuição. 
    
3. Chame o método de **IABContainer::GetContentsTable** da lista de distribuição para acessar sua tabela de conteúdo. 
    
4. Chame [HrQueryAllRows](hrqueryallrows.md) para recuperar todas as linhas da tabela que representa os membros da lista de distribuição. 
    

