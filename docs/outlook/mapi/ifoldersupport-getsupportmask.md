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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6f7aa23606da40c817c9af623b8bade9383ce427
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766928"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="77546-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="77546-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="77546-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77546-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77546-105">Obtém informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="77546-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="77546-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77546-106">Parameters</span></span>

 <span data-ttu-id="77546-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="77546-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="77546-108">[out] Uma máscara de bits que indica se a pasta oferece suporte a compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="77546-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="77546-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="77546-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="77546-110">Indica que a pasta não oferece suporte a compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="77546-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="77546-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="77546-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="77546-112">Indica que a pasta suporta compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="77546-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77546-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="77546-113">Return value</span></span>

<span data-ttu-id="77546-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="77546-114">S_OK</span></span> 
  
> <span data-ttu-id="77546-115">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="77546-115">The call was successful.</span></span>
    

