---
title: IAttachmentSecurityIsAttachmentBlocked
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity.IsAttachmentBlocked
api_type:
- COM
ms.assetid: 6986d27a-9602-e44a-0797-4c47f2184ef7
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 45e4362fc025c1784e9432c5d641e865a044bd00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766903"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="a0179-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="a0179-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="a0179-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0179-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0179-105">Verifica se um anexo especificado será bloqueado pelo Microsoft Outlook 2010 ou o Microsoft Outlook 2013 para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="a0179-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="a0179-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="a0179-106">Parameters</span></span>

 <span data-ttu-id="a0179-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="a0179-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="a0179-108">[in] Ponteiro para o nome de arquivo de anexo.</span><span class="sxs-lookup"><span data-stu-id="a0179-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="a0179-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="a0179-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="a0179-110">[out] Ponteiro para um valor que indica **true** se o anexo especificado está bloqueado; Caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a0179-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a0179-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0179-111">See also</span></span>



[<span data-ttu-id="a0179-112">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="a0179-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a0179-113">Verifique se que um anexo estiver bloqueado</span><span class="sxs-lookup"><span data-stu-id="a0179-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

