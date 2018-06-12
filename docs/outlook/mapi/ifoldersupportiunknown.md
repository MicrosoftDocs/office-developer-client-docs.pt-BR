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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a4a1c78e65d9a515b2b42d7e0a2bc3a8b4bd8869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766958"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="df78b-103">IFolderSupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="df78b-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="df78b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df78b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df78b-105">Fornece informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="df78b-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df78b-106">Provided by:</span><span class="sxs-lookup"><span data-stu-id="df78b-106">Provided by:</span></span>  <br/> |<span data-ttu-id="df78b-107">Provedor de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="df78b-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="df78b-108">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="df78b-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="df78b-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="df78b-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="df78b-110">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="df78b-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df78b-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="df78b-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="df78b-112">Obtém informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="df78b-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df78b-113">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="df78b-113">Remarks</span></span>

<span data-ttu-id="df78b-114">Geralmente, o Microsoft Office Outlook requer um MAPI armazenar provedor implemente essa interface se o provedor quer compartilhar uma pasta.</span><span class="sxs-lookup"><span data-stu-id="df78b-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="df78b-115">A exceção é o provedor de repositório do Exchange Server, que pode compartilhar pastas sem implementar esta interface.</span><span class="sxs-lookup"><span data-stu-id="df78b-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="df78b-116">Um cliente pode consultar um **[IMAPIFolder](imapifolderimapicontainer.md)** **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="df78b-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="df78b-117">Se tiver êxito, chame **IFolderSupport::GetSupportMask** e procurar estará definido o bit **FS_SUPPORTS_SHARING** a ser definido.</span><span class="sxs-lookup"><span data-stu-id="df78b-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

