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
ms.openlocfilehash: d255d7b6e80fe0c080fa0a27a7976db758a8c2ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439776"
---
# <a name="iattachmentsecurityisattachmentblocked"></a><span data-ttu-id="e47a9-103">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="e47a9-103">IAttachmentSecurity::IsAttachmentBlocked</span></span>

  
  
<span data-ttu-id="e47a9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e47a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e47a9-105">Verifica se um anexo especificado está bloqueado pelo Microsoft Outlook 2010 ou Microsoft Outlook 2013 para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="e47a9-105">Checks if a specified attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span>
  
```cpp
HRESULT IAttachmentSecurity::IsAttachmentBlocked( 
    LPCWSTR pwszFileName,  
    BOOL *pfBlocked 
);
```

## <a name="parameters"></a><span data-ttu-id="e47a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e47a9-106">Parameters</span></span>

 <span data-ttu-id="e47a9-107">_pwszFileName_</span><span class="sxs-lookup"><span data-stu-id="e47a9-107">_pwszFileName_</span></span>
  
> <span data-ttu-id="e47a9-108">no Ponteiro para o nome de arquivo de um anexo.</span><span class="sxs-lookup"><span data-stu-id="e47a9-108">[in] Pointer to the filename of an attachment.</span></span>
    
 <span data-ttu-id="e47a9-109">_pfBlocked_</span><span class="sxs-lookup"><span data-stu-id="e47a9-109">_pfBlocked_</span></span>
  
> <span data-ttu-id="e47a9-110">bota Ponteiro para um valor que indica **true** se o anexo especificado estiver bloqueado; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e47a9-110">[out] Pointer to a value indicating **true** if the specified attachment is blocked; otherwise, **false**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e47a9-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="e47a9-111">See also</span></span>



[<span data-ttu-id="e47a9-112">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="e47a9-112">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e47a9-113">Verificar se um anexo está bloqueado</span><span class="sxs-lookup"><span data-stu-id="e47a9-113">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

