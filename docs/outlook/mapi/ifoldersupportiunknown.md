---
title: IFolderSupport IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport
api_type:
- COM
ms.assetid: a4b03a66-cf6d-cd20-f1df-b247d3ee87aa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d17de9cc11bd791c75b83093a0431c138fd606d6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564168"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="6b898-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b898-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="6b898-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b898-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b898-105">Fornece informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6b898-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6b898-106">Provided by:</span><span class="sxs-lookup"><span data-stu-id="6b898-106">Provided by:</span></span>  <br/> |<span data-ttu-id="6b898-107">Provedor de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="6b898-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="6b898-108">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="6b898-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6b898-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="6b898-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6b898-110">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="6b898-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b898-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="6b898-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="6b898-112">Obtém informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6b898-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b898-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b898-113">Remarks</span></span>

<span data-ttu-id="6b898-114">Geralmente, o Microsoft Office Outlook requer um MAPI armazenar provedor implemente essa interface se o provedor quer compartilhar uma pasta.</span><span class="sxs-lookup"><span data-stu-id="6b898-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="6b898-115">A exceção é o provedor de repositório do Exchange Server, que pode compartilhar pastas sem implementar esta interface.</span><span class="sxs-lookup"><span data-stu-id="6b898-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="6b898-116">Um cliente pode consultar um **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="6b898-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="6b898-117">Se tiver êxito, chame **IFolderSupport::GetSupportMask** e procurar estará definido o bit **FS_SUPPORTS_SHARING** a ser definido.</span><span class="sxs-lookup"><span data-stu-id="6b898-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

