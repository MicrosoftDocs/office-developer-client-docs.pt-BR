---
title: Tipos de endereço MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eee97982-29be-4dcf-ae11-8a38f0080ea7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b0ff4ecff7a6e834f1e017adc11244657896db03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405433"
---
# <a name="mapi-address-types"></a>Tipos de endereço MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cada usuário de mensagens é associado a um tipo de endereço, uma cadeia de caracteres que descreve o formato do endereço do usuário armazenado na propriedade **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)). Os tipos de endereço mapeiam para formatos de endereço. Ou seja, ao olhar para o tipo de endereço de um destinatário, os aplicativos cliente podem determinar como formatar um endereço apropriado para o destinatário. 
  
Por exemplo, o  `SMTP` tipo de endereço especifica o endereço padrão da Internet: 
  
 `username@companyname.com.`
  
E o tipo  `EX` de endereço especifica um endereço do Exchange Server. 
  
Todas as entradas do livro de endereços devem ter um tipo de endereço válido. Os clientes exigem que seus usuários especifiquem um tipo de endereço ao criar um tipo de destinatário personalizado sem suporte do provedor de agendas. Para as entradas com suporte, os provedores de agendas são necessários para fornecer tipos de endereço válidos. 
  
MAPI define apenas um tipo de endereço: MAPIPDL, que significa lista de distribuição pessoal.
  
Para obter uma lista dos tipos de endereços suportados por todos os provedores de transporte na sessão, os aplicativos cliente chamam o método **IMAPISession::EnumAdrTypes.** Para obter mais informações, [consulte IMAPISession::EnumAdrTypes](imapisession-enumadrtypes.md).
  

