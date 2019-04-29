---
title: Tabelas de informações associadas à pasta
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
# <a name="folder-associated-information-tables"></a>Tabelas de informações associadas à pasta

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI define o sinalizador MAPI_ASSOCIATED para vários componentes MAPI a serem usados ao lidar com tabelas de informações associadas. Cada pasta em um repositório de mensagens deve ter uma tabela de conteúdo associada junto com sua tabela de conteúdo padrão. Os aplicativos cliente armazenam mensagens especiais em uma tabela de conteúdo associada da pasta para conter formulários e exibições. Na verdade, para dar suporte a formulários e modos de exibição, seu provedor de repositório de mensagens deve implementar tabelas de conteúdo associadas.
  
Para implementar tabelas de conteúdo associadas, seu provedor de repositório deve fazer o seguinte:
  
- Suporte para o sinalizador MAPI_ASSOCIATED no método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable para que os aplicativos clientes possam obter a tabela de conteúdo associada da pasta em vez da tabela de conteúdo padrão. 
    
- Suporta o sinalizador MAPI_ASSOCIATED no método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para que os aplicativos clientes possam adicionar mensagens à tabela de conteúdo associada de uma pasta. 
    
- Defina o bit MAPI_ACCESS_CREATE_ASSOCIATED na propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) em objetos Folder.
    
- Suporta o sinalizador DEL_ASSOCIATED no método [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) . 
    
- Defina o bit MSGFLAG_ASSOCIATED na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para mensagens na tabela de conteúdo associado.
    
- Expor e responder à propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) em Folders.
    
- Mantenha a propriedade **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) em Folders.
    
Não há nenhum bit na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar se o seu provedor de repositório de mensagens oferece suporte a tabelas de conteúdo associadas. Se o seu provedor de repositório de mensagens não oferecer suporte a eles, ele deverá retornar MAPI_E_NO_SUPPORT quando os aplicativos cliente chamarem qualquer um dos métodos acima com o sinalizador MAPI_ASSOCIATED.
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

