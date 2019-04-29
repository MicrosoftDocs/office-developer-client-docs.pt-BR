---
title: Exibir a caixa de diálogo endereço comum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 812c850d1fcb6d3712d76b160b56b839b2e1353d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436899"
---
# <a name="displaying-the-common-address-dialog-box"></a>Exibir a caixa de diálogo endereço comum

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A caixa de diálogo endereço comum MAPI pode ser usada para uma variedade de tarefas de endereçamento, como criar uma lista de destinatários. Para exibir essa caixa de diálogo, chame **IAddrBook:: address**. Dependendo de qual dos vários parâmetros você definiu e como você os definiu, é possível limitar a exibição a entradas de um tipo específico de um determinado contêiner.
  
 **Para limitar a caixa de diálogo Endereço para exibir somente as entradas do catálogo de endereços pessoal (PAB)**
  
1. Chame [IAddrBook:: GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB. 
    
2. Crie uma restrição de propriedade que use RELOP_EQ para o membro **RELOP** da estrutura [SPropertyRestriction](spropertyrestriction.md) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como o membro **ulPropTag** . Se você usar **PR_ENTRYID**, passe o identificador de entrada recuperado do **GetPAB**. Se você usar **PR_AB_PROVIDER_ID**, passe o valor incluído no MSPAB. Arquivo de cabeçalho H. **PR_AB_PROVIDER_ID** é o identificador exclusivo do PAB criado por MAPI. 
    
3. Chame [IAddrBook:: address](iaddrbook-address.md) com o parâmetro _lpHierRestriction_ apontando para a restrição de propriedade. 
    

