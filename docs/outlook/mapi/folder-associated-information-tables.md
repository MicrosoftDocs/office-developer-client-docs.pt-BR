---
title: Folder-Associated de Informações do Folder-Associated
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b72a0d36-c489-41d6-af57-72fbf4b7a3f5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2332c2a2f7eb46816eab5305b73344e25b2832d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426412"
---
# <a name="folder-associated-information-tables"></a>Folder-Associated de Informações do Folder-Associated

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define o sinalizador MAPI_ASSOCIATED para vários componentes MAPI a ser usado ao lidar com tabelas de informações associadas. Cada pasta em um armazenamento de mensagens deve ter uma tabela de conteúdo associada juntamente com sua tabela de conteúdo padrão. Os aplicativos cliente armazenam mensagens especiais na tabela de conteúdo associada de uma pasta para armazenar formulários e exibições. Na verdade, para dar suporte a formulários e exibições, seu provedor de armazenamento de mensagens deve implementar tabelas de conteúdo associadas.
  
Para implementar tabelas de conteúdo associadas, seu provedor de armazenamento deve fazer o seguinte:
  
- Suporte ao sinalizador MAPI_ASSOCIATED no método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para que os aplicativos cliente possam obter a tabela de conteúdo associada da pasta em vez da tabela de conteúdo padrão. 
    
- Suporte ao MAPI_ASSOCIATED sinalizador no método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que os aplicativos cliente possam adicionar mensagens à tabela de conteúdo associada de uma pasta. 
    
- De definida MAPI_ACCESS_CREATE_ASSOCIATED bit **na propriedade PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) em objetos folder.
    
- Suporte ao DEL_ASSOCIATED no método [IMAPIFolder::EmptyFolder.](imapifolder-emptyfolder.md) 
    
- Defina MSGFLAG_ASSOCIATED bit na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para mensagens na tabela de conteúdo associada.
    
- Expor e responder à **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) em pastas.
    
- Mantenha a **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) em pastas.
    
Não há bit na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar se seu provedor de repositório de mensagens oferece suporte a tabelas de conteúdo associadas. Se seu provedor de armazenamento de mensagens não os suportar, ele deverá retornar MAPI_E_NO_SUPPORT quando os aplicativos cliente chamarem qualquer um dos métodos acima com o sinalizador MAPI_ASSOCIATED mensagem.
  
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

