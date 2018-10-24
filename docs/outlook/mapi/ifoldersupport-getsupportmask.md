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
ms.openlocfilehash: c51f4a7266e67be08f31daa5afbf23ce0b256252
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567850"
---
# <a name="ifoldersupportgetsupportmask"></a><span data-ttu-id="3e8b3-103">IFolderSupport::GetSupportMask</span><span class="sxs-lookup"><span data-stu-id="3e8b3-103">IFolderSupport::GetSupportMask</span></span>

  
  
<span data-ttu-id="3e8b3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3e8b3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3e8b3-105">Obtém informações sobre o suporte de uma pasta para compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b3-105">Gets information about a folder's support for sharing.</span></span>
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a><span data-ttu-id="3e8b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e8b3-106">Parameters</span></span>

 <span data-ttu-id="3e8b3-107">_pdwSupportMask_</span><span class="sxs-lookup"><span data-stu-id="3e8b3-107">_pdwSupportMask_</span></span>
  
> <span data-ttu-id="3e8b3-108">[out] Uma máscara de bits que indica se a pasta oferece suporte a compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b3-108">[out] A bitmask indicating if the folder supports sharing.</span></span>
    
 <span data-ttu-id="3e8b3-109">**FS_NONE**</span><span class="sxs-lookup"><span data-stu-id="3e8b3-109">**FS_NONE**</span></span>
  
> <span data-ttu-id="3e8b3-110">Indica que a pasta não oferece suporte a compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b3-110">Indicates that the folder does not support sharing.</span></span>
    
 <span data-ttu-id="3e8b3-111">**FS_SUPPORTS_SHARING**</span><span class="sxs-lookup"><span data-stu-id="3e8b3-111">**FS_SUPPORTS_SHARING**</span></span>
  
> <span data-ttu-id="3e8b3-112">Indica que a pasta suporta compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="3e8b3-112">Indicates that the folder supports sharing.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3e8b3-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="3e8b3-113">Return value</span></span>

<span data-ttu-id="3e8b3-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3e8b3-114">S_OK</span></span> 
  
> <span data-ttu-id="3e8b3-115">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3e8b3-115">The call was successful.</span></span>
    

