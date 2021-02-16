---
title: Suporte a texto RTF para provedores de armazenamento de mensagens
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
# <a name="supporting-rtf-text-for-message-store-providers"></a>Suporte a texto RTF para provedores de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Alguns aplicativos cliente permitem que os usuários usem texto RTF (Rich Text Format) em suas mensagens. Se seu provedor de armazenamento de mensagens precisar dar suporte a texto RTF em mensagens, ele precisará manipular a propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), além da propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Primarily, this means storing both properties, and making sure **that PR_BODY** contains a plain text version of the text in **PR_RTF_COMPRESSED**. A [função RTFSync](rtfsync.md) é útil para essa finalidade. 
  
Há dois sinalizadores que podem ser definidos na propriedade **PR_STORE_SUPPORT_MASK** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)do objeto de repositório de mensagens que dizem aos clientes o que eles podem esperar do provedor de repositório de mensagens com relação às propriedades **PR_BODY** e **PR_RTF_COMPRESSED** em mensagens no repositório de mensagens. O STORE_RTF_OK sinalizador indica que o armazenamento pode gerar o valor da propriedade **PR_BODY a** partir da propriedade **PR_RTF_COMPRESSED dinamicamente,** o que libera os clientes da carga de sincronize-los explicitamente. O STORE_UNCOMPRESSED_RTF sinalizador indica que o provedor de armazenamento de mensagens pode dar suporte a dados não **compactados PR_RTF_COMPRESSED**.
  
Provedores de armazenamento de mensagens que não suportam texto RTF precisam excluir PR_RTF_IN_SYNC propriedade **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) quando a propriedade PR_BODY é mudada **para** interoperar corretamente com aplicativos cliente que não suportam texto RTF. 
  
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

