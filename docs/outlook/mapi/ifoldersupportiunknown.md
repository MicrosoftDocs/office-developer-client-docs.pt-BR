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
ms.openlocfilehash: da186e6804fc3d3c820551fee66519a2ff76f0db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351384"
---
# <a name="ifoldersupport--iunknown"></a><span data-ttu-id="7fb15-103">IFolderSupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7fb15-103">IFolderSupport : IUnknown</span></span>

  
  
<span data-ttu-id="7fb15-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fb15-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fb15-105">Fornece informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7fb15-105">Provides information about a folder's support for sharing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7fb15-106">Provided by:</span><span class="sxs-lookup"><span data-stu-id="7fb15-106">Provided by:</span></span>  <br/> |<span data-ttu-id="7fb15-107">Provedor de repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="7fb15-107">Message store provider</span></span>  <br/> |
|<span data-ttu-id="7fb15-108">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="7fb15-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7fb15-109">IID_IFolderSupport</span><span class="sxs-lookup"><span data-stu-id="7fb15-109">IID_IFolderSupport</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7fb15-110">Vtable order</span><span class="sxs-lookup"><span data-stu-id="7fb15-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7fb15-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span><span class="sxs-lookup"><span data-stu-id="7fb15-111">**[GetSupportMask](ifoldersupport-getsupportmask.md)**</span></span> <br/> |<span data-ttu-id="7fb15-112">Obtém informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="7fb15-112">Gets information about a folder's support for sharing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7fb15-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7fb15-113">Remarks</span></span>

<span data-ttu-id="7fb15-114">Geralmente, o Microsoft Office Outlook requer um provedor de repositório MAPI para implementar essa interface se o provedor quiser compartilhar uma pasta.</span><span class="sxs-lookup"><span data-stu-id="7fb15-114">Generally, Microsoft Office Outlook requires a MAPI store provider to implement this interface if the provider wants to share a folder.</span></span> <span data-ttu-id="7fb15-115">A exceção é o provedor de armazenamento do Exchange Server, que pode compartilhar pastas sem implementar esta interface.</span><span class="sxs-lookup"><span data-stu-id="7fb15-115">The exception is the Exchange Server store provider, which can share folders without implementing this interface.</span></span>
  
<span data-ttu-id="7fb15-116">Um cliente pode consultar um **[IMAPIFolder](imapifolderimapicontainer.md)** para **IFolderSupport**.</span><span class="sxs-lookup"><span data-stu-id="7fb15-116">A client can query an **[IMAPIFolder](imapifolderimapicontainer.md)** for **IFolderSupport**.</span></span> <span data-ttu-id="7fb15-117">Se isso tiver êxito, chame **IFolderSupport:: GetSupportMask** e verifique o bit de **FS_SUPPORTS_SHARING** a ser definido.</span><span class="sxs-lookup"><span data-stu-id="7fb15-117">If that succeeds, call **IFolderSupport::GetSupportMask** and check for the **FS_SUPPORTS_SHARING** bit to be set.</span></span> 
  

