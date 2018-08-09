---
title: Tabelas de informações associadas à pasta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 09cac591aac9d266571348531e378974b86a3a9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766580"
---
# <a name="folder-associated-information-tables"></a>Tabelas de informações associadas à pasta

  
  
**Aplica-se a**: Outlook 
  
MAPI define o sinalizador MAPI_ASSOCIATED de vários componentes MAPI para usar quando lidando com as tabelas de informações associadas. Cada pasta em um repositório de mensagem deve ter uma tabela de conteúdo associado, juntamente com sua tabela de conteúdo padrão. Aplicativos cliente armazenam mensagens especiais na tabela de conteúdo associado de uma pasta para armazenar formulários e modos de exibição. Na verdade, para dar suporte a formulários e modos de exibição, seu provedor de armazenamento de mensagem deve implementar as tabelas de conteúdo associado.
  
Para implementar as tabelas de conteúdo associado, seu provedor de armazenamento deve fazer o seguinte:
  
- Suporta o sinalizador MAPI_ASSOCIATED no método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para que aplicativos cliente podem obter tabela de conteúdo associado da pasta no lugar do índice de conteúdo padrão. 
    
- Suporta o sinalizador MAPI_ASSOCIATED no método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que aplicativos cliente podem adicionar mensagens à tabela de conteúdo associado de uma pasta. 
    
- Defina o bit MAPI_ACCESS_CREATE_ASSOCIATED na propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) em objetos de pasta.
    
- Suporta o sinalizador DEL_ASSOCIATED no método [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Defina o MSGFLAG_ASSOCIATED bit na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para mensagens na tabela de conteúdo associado.
    
- Expor e responder à propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) em pastas.
    
- Manter a propriedade **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) em pastas.
    
Não há nenhum bit na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar se o seu provedor de armazenamento de mensagens oferece suporte a tabelas de conteúdo associado. Se o seu provedor de armazenamento de mensagem não oferecer suporte a eles, ele deverá retornar MAPI_E_NO_SUPPORT quando os aplicativos cliente chamam qualquer um dos métodos acima com o sinalizador MAPI_ASSOCIATED.
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

