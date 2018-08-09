---
title: Exibir a caixa de diálogo de endereços comuns
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 276f9fa8-c333-4381-b20f-22fe9d2f27cd
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a7b603504956be9ec3066e5ff5e1d5db7d59852a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766453"
---
# <a name="displaying-the-common-address-dialog-box"></a>Exibir a caixa de diálogo de endereços comuns

  
  
**Aplica-se a**: Outlook 
  
A caixa de diálogo de endereço comuns do MAPI pode ser usada para uma variedade de tarefas de endereçamento como construir uma lista de destinatários. Para exibir esta caixa de diálogo, chame **IAddrBook::Address**. Dependendo de qual dos vários parâmetros que você definir e como defini-las, é possível limitar o seu vídeo às entradas de um determinado tipo de um contêiner específico.
  
 **Para limitar a caixa de diálogo de endereço para exibindo apenas entradas de catálogo (PAB) particular de endereços**
  
1. Chame [IAddrBook::GetPAB](iaddrbook-getpab.md) para recuperar o identificador de entrada do PAB. 
    
2. Criar uma restrição de propriedade que usa RELOP_EQ para o membro **relop** da estrutura de [SPropertyRestriction](spropertyrestriction.md) e **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) ou **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) como o membro **ulPropTag** . Se você usar **PR_ENTRYID**, passe o identificador de entrada recuperado do **GetPAB**. Se você usar **PR_AB_PROVIDER_ID**, passe o valor incluído no MSPAB. Arquivo de cabeçalho H. **PR_AB_PROVIDER_ID** é o identificador exclusivo para o PAB projetado pela MAPI. 
    
3. Chame [IAddrBook::Address](iaddrbook-address.md) com o parâmetro _lpHierRestriction_ apontando para a restrição de propriedade. 
    

