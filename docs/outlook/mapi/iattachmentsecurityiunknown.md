---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411411"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="96057-103">IAttachmentSecurity : IUnknown</span><span class="sxs-lookup"><span data-stu-id="96057-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="96057-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96057-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96057-105">Permite que as soluções do Microsoft Outlook 2010 e do Microsoft Outlook 2013 descubram se um anexo é considerado não seguro e bloqueado para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="96057-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="96057-106">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="96057-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="96057-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="96057-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="96057-108">Vtable order</span><span class="sxs-lookup"><span data-stu-id="96057-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="96057-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="96057-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="96057-110">Verifica se um anexo especificado está bloqueado pelo Outlook 2010 ou pelo Outlook 2013 para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="96057-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96057-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="96057-111">Remarks</span></span>

<span data-ttu-id="96057-112">As soluções do Outlook 2010 e do Outlook 2013 podem consultar essa interface para ver se um anexo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="96057-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="96057-113">Os anexos bloqueados pelo Outlook 2010 ou pelo Outlook 2013 variam dependendo de como o Outlook 2010 ou o Outlook 2013 foi configurado e as políticas que um administrador aplicou.</span><span class="sxs-lookup"><span data-stu-id="96057-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="96057-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="96057-114">See also</span></span>



[<span data-ttu-id="96057-115">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="96057-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="96057-116">Verificar se um anexo está bloqueado</span><span class="sxs-lookup"><span data-stu-id="96057-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

