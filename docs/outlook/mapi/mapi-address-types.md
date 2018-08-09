---
title: Tipos de endereço MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 20eb429b2574f67e8b28ae96eeb96f42840123d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767804"
---
# <a name="mapi-address-types"></a>Tipos de endereço MAPI

  
  
**Aplica-se a**: Outlook 
  
Cada usuário de mensagens é associado um tipo de endereço, uma cadeia de caracteres que descreve o formato do endereço do usuário que está armazenado na propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Tipos de endereço são mapeados para formatos de endereço. Ou seja, examinando o tipo de endereço do destinatário, aplicativos cliente podem determinar como formatar um endereço apropriado para o destinatário. 
  
Por exemplo, o `SMTP` tipo de endereço Especifica o endereço de Internet padrão: 
  
 `username@companyname.com.`
  
E, o `EX` tipo de endereço Especifica um endereço de servidor do Exchange. 
  
Todas as entradas do catálogo de endereços devem ter um tipo de endereço válido. Os clientes precisam de seus usuários especificar um tipo de endereço ao criar um tipo de destinatário personalizado sem suporte pelo provedor de catálogo de endereços. Para as entradas que oferecem suporte a eles, provedores de catálogo de endereços são necessárias para fornecer tipos de endereço válido. 
  
MAPI define o tipo de apenas um endereço: MAPIPDL, o que significa de lista de distribuição pessoal.
  
Para obter uma lista dos tipos de endereço suportado por todos os provedores de transporte da sessão, os aplicativos cliente chamam o método de **IMAPISession::EnumAdrTypes** . Para obter mais informações, consulte [IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  
