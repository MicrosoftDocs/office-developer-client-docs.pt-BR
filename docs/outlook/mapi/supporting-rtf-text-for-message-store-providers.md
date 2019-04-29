---
title: Suporte a texto RTF para provedores de repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: dc1d8a5e237b7b34f3a57e9789e03e2f16237764
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414211"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Suporte a texto RTF para provedores de repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns aplicativos cliente permitem que os usuários usem texto em formato Rich Text (RTF) em suas mensagens. Se o seu provedor de repositório de mensagens precisa suportar texto RTF em mensagens, ele precisa manipular a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), além da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Basicamente, isso significa armazenar as duas propriedades e certificar-se de que **PR_BODY** contém uma versão de texto sem formatação do texto no **PR_RTF_COMPRESSED**. A função [RTFSync](rtfsync.md) é útil para essa finalidade. 
  
Há dois sinalizadores que podem ser definidos na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto Message Store que informa aos clientes o que eles podem esperar do provedor de armazenamento de mensagens em relação ao **PR_BODY** e ao **PR_ RTF_COMPRESSED** Propriedades em mensagens no repositório de mensagens. O sinalizador STORE_RTF_OK indica que o repositório pode gerar o valor da propriedade **PR_BODY** da propriedade **PR_RTF_COMPRESSED** dinamicamente, o que alivia os clientes do ônus de sincronizá-los explicitamente. O sinalizador STORE_UNCOMPRESSED_RTF indica que o provedor de repositório de mensagens pode dar suporte a dados não compactados no **PR_RTF_COMPRESSED**.
  
Provedores de repositório de mensagens que não dão suporte a texto RTF precisam excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) quando a propriedade **PR_BODY** é alterada para interoperar corretamente com aplicativos clientes que oferecem suporte a texto RTF . 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

