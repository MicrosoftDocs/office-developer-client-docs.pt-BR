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
ms.openlocfilehash: 9c9c75d0ae4b9fe060d6717dfa11ad418cbb715b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564644"
---
# <a name="folder-associated-information-tables"></a><span data-ttu-id="2d57a-103">Tabelas de informações associadas à pasta</span><span class="sxs-lookup"><span data-stu-id="2d57a-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="2d57a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d57a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d57a-105">MAPI define o sinalizador MAPI_ASSOCIATED de vários componentes MAPI para usar quando lidando com as tabelas de informações associadas.</span><span class="sxs-lookup"><span data-stu-id="2d57a-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="2d57a-106">Cada pasta em um repositório de mensagem deve ter uma tabela de conteúdo associado, juntamente com sua tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="2d57a-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="2d57a-107">Aplicativos cliente armazenam mensagens especiais na tabela de conteúdo associado de uma pasta para armazenar formulários e modos de exibição.</span><span class="sxs-lookup"><span data-stu-id="2d57a-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="2d57a-108">Na verdade, para dar suporte a formulários e modos de exibição, seu provedor de armazenamento de mensagem deve implementar as tabelas de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="2d57a-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="2d57a-109">Para implementar as tabelas de conteúdo associado, seu provedor de armazenamento deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2d57a-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="2d57a-110">Suporta o sinalizador MAPI_ASSOCIATED no método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) para que aplicativos cliente podem obter tabela de conteúdo associado da pasta no lugar do índice de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="2d57a-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="2d57a-111">Suporta o sinalizador MAPI_ASSOCIATED no método [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) para que aplicativos cliente podem adicionar mensagens à tabela de conteúdo associado de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2d57a-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="2d57a-112">Defina o bit MAPI_ACCESS_CREATE_ASSOCIATED na propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) em objetos de pasta.</span><span class="sxs-lookup"><span data-stu-id="2d57a-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="2d57a-113">Suporta o sinalizador DEL_ASSOCIATED no método [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="2d57a-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="2d57a-114">Defina o MSGFLAG_ASSOCIATED bit na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para mensagens na tabela de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="2d57a-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="2d57a-115">Expor e responder à propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) em pastas.</span><span class="sxs-lookup"><span data-stu-id="2d57a-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="2d57a-116">Manter a propriedade **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) em pastas.</span><span class="sxs-lookup"><span data-stu-id="2d57a-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="2d57a-117">Não há nenhum bit na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar se o seu provedor de armazenamento de mensagens oferece suporte a tabelas de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="2d57a-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="2d57a-118">Se o seu provedor de armazenamento de mensagem não oferecer suporte a eles, ele deverá retornar MAPI_E_NO_SUPPORT quando os aplicativos cliente chamam qualquer um dos métodos acima com o sinalizador MAPI_ASSOCIATED.</span><span class="sxs-lookup"><span data-stu-id="2d57a-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2d57a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d57a-119">See also</span></span>



[<span data-ttu-id="2d57a-120">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="2d57a-120">Message Store Features</span></span>](message-store-features.md)

