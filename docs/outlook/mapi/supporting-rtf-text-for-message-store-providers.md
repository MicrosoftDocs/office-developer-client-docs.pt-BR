---
title: Suporte a texto RTF para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0022fe70-cf11-49a5-9c97-a6bc5b5b13aa
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d7d64c8a7d4df4898502f4574ca879c736547b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770562"
---
# <a name="supporting-rtf-text-for-message-store-providers"></a>Suporte a texto RTF para provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 
  
Alguns aplicativos de cliente permitem que os usuários utilizem o formato Rich Text (RTF) texto em suas mensagens. Se sua mensagem armazenar as necessidades do provedor para dar suporte ao texto RTF em mensagens, ele precisa lidar com a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), além da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Basicamente, isso significa armazenar ambas as propriedades e certificando-se de que **PR_BODY** contém uma versão de texto sem formatação do texto em **PR_RTF_COMPRESSED**. A função [RTFSync](rtfsync.md) é útil para essa finalidade. 
  
Há dois sinalizadores que podem ser definidos na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do objeto repositório de mensagens que informam os clientes que eles podem esperar do provedor de repositório de mensagem com relação a **PR_BODY** e **PR_ RTF_COMPRESSED** propriedades em mensagens no repositório de mensagem. O sinalizador STORE_RTF_OK indica que o repositório pode gerar o valor da propriedade **PR_BODY** da propriedade **PR_RTF_COMPRESSED** dinamicamente, que libera os clientes da carga de sincronizá-los explicitamente. O sinalizador STORE_UNCOMPRESSED_RTF indica que o provedor de armazenamento de mensagens pode oferecer suporte a dados descompactados em **PR_RTF_COMPRESSED**.
  
Provedores de armazenamento de mensagem que não têm suporte para texto RTF necessário excluir a propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) quando a propriedade **PR_BODY** é alterada para adequadamente interoperar com os aplicativos cliente que têm suporte para texto RTF . 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

