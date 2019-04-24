---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1c27bdc52ebe725c40cbf318fab0678f41cdc287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350831"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="e5111-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="e5111-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="e5111-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5111-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5111-105">Obtém informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e5111-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="e5111-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5111-106">Parameters</span></span>

 <span data-ttu-id="e5111-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="e5111-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="e5111-108">bota Uma bitmask indicando se a pasta oferece suporte ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e5111-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="e5111-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="e5111-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="e5111-110">Indica que a pasta não tem suporte para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e5111-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="e5111-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="e5111-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="e5111-112">Indica que a pasta oferece suporte ao compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e5111-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e5111-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e5111-113">Return value</span></span>

<span data-ttu-id="e5111-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="e5111-114">S_OK</span></span> 
  
> <span data-ttu-id="e5111-115">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e5111-115">The call was successful.</span></span>
    

