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
# <a name="folder-associated-information-tables"></a><span data-ttu-id="b2832-103">Tabelas de informações associadas à pasta</span><span class="sxs-lookup"><span data-stu-id="b2832-103">Folder-Associated Information Tables</span></span>

  
  
<span data-ttu-id="b2832-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2832-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2832-105">MAPI define o sinalizador MAPI_ASSOCIATED para vários componentes MAPI a serem usados ao lidar com tabelas de informações associadas.</span><span class="sxs-lookup"><span data-stu-id="b2832-105">MAPI defines the MAPI_ASSOCIATED flag for various MAPI components to use when dealing with associated information tables.</span></span> <span data-ttu-id="b2832-106">Cada pasta em um repositório de mensagens deve ter uma tabela de conteúdo associada junto com sua tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="b2832-106">Each folder in a message store should have an associated contents table along with its standard contents table.</span></span> <span data-ttu-id="b2832-107">Os aplicativos cliente armazenam mensagens especiais em uma tabela de conteúdo associada da pasta para conter formulários e exibições.</span><span class="sxs-lookup"><span data-stu-id="b2832-107">Client applications store special messages in a folder's associated contents table to hold forms and views.</span></span> <span data-ttu-id="b2832-108">Na verdade, para dar suporte a formulários e modos de exibição, seu provedor de repositório de mensagens deve implementar tabelas de conteúdo associadas.</span><span class="sxs-lookup"><span data-stu-id="b2832-108">In fact, to support forms and views, your message store provider must implement associated contents tables.</span></span>
  
<span data-ttu-id="b2832-109">Para implementar tabelas de conteúdo associadas, seu provedor de repositório deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b2832-109">To implement associated contents tables, your store provider must do the following:</span></span>
  
- <span data-ttu-id="b2832-110">Suporte para o sinalizador MAPI_ASSOCIATED no método [IMAPIContainer::](imapicontainer-getcontentstable.md) getcontenttable para que os aplicativos clientes possam obter a tabela de conteúdo associada da pasta em vez da tabela de conteúdo padrão.</span><span class="sxs-lookup"><span data-stu-id="b2832-110">Support the MAPI_ASSOCIATED flag in the [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) method so client applications can get the folder's associated contents table instead of the standard contents table.</span></span> 
    
- <span data-ttu-id="b2832-111">Suporta o sinalizador MAPI_ASSOCIATED no método [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) para que os aplicativos clientes possam adicionar mensagens à tabela de conteúdo associada de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="b2832-111">Support the MAPI_ASSOCIATED flag in the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method so client applications can add messages to a folder's associated contents table.</span></span> 
    
- <span data-ttu-id="b2832-112">Defina o bit MAPI_ACCESS_CREATE_ASSOCIATED na propriedade **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) em objetos Folder.</span><span class="sxs-lookup"><span data-stu-id="b2832-112">Set the MAPI_ACCESS_CREATE_ASSOCIATED bit in the **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) property on folder objects.</span></span>
    
- <span data-ttu-id="b2832-113">Suporta o sinalizador DEL_ASSOCIATED no método [IMAPIFolder:: EmptyFolder](imapifolder-emptyfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="b2832-113">Support the DEL_ASSOCIATED flag in the [IMAPIFolder::EmptyFolder](imapifolder-emptyfolder.md) method.</span></span> 
    
- <span data-ttu-id="b2832-114">Defina o bit MSGFLAG_ASSOCIATED na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) para mensagens na tabela de conteúdo associado.</span><span class="sxs-lookup"><span data-stu-id="b2832-114">Set the MSGFLAG_ASSOCIATED bit in the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property for messages in the associated contents table.</span></span>
    
- <span data-ttu-id="b2832-115">Expor e responder à propriedade **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) em Folders.</span><span class="sxs-lookup"><span data-stu-id="b2832-115">Expose and respond to the **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)) property on folders.</span></span>
    
- <span data-ttu-id="b2832-116">Mantenha a propriedade **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) em Folders.</span><span class="sxs-lookup"><span data-stu-id="b2832-116">Maintain the **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)) property on folders.</span></span>
    
<span data-ttu-id="b2832-117">Não há nenhum bit na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) para indicar se o seu provedor de repositório de mensagens oferece suporte a tabelas de conteúdo associadas.</span><span class="sxs-lookup"><span data-stu-id="b2832-117">There is no bit in the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property to indicate whether your message store provider supports associated contents tables.</span></span> <span data-ttu-id="b2832-118">Se o seu provedor de repositório de mensagens não oferecer suporte a eles, ele deverá retornar MAPI_E_NO_SUPPORT quando os aplicativos cliente chamarem qualquer um dos métodos acima com o sinalizador MAPI_ASSOCIATED.</span><span class="sxs-lookup"><span data-stu-id="b2832-118">If your message store provider does not support them, it should return MAPI_E_NO_SUPPORT when client applications call any of the above methods with the MAPI_ASSOCIATED flag.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b2832-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2832-119">See also</span></span>



[<span data-ttu-id="b2832-120">Recursos do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="b2832-120">Message Store Features</span></span>](message-store-features.md)

