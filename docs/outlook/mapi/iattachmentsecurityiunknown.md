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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 040be6cea64dd58e23d79c20a9ae9dddf02fa87d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766883"
---
# <a name="iattachmentsecurity--iunknown"></a><span data-ttu-id="fe514-103">IAttachmentSecurity: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fe514-103">IAttachmentSecurity : IUnknown</span></span>

  
  
<span data-ttu-id="fe514-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe514-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe514-105">Permite que as soluções do Microsoft Outlook 2010 e o Microsoft Outlook 2013 descobrir se um anexo é considerado não seguros e bloqueados para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="fe514-105">Allows Microsoft Outlook 2010 and Microsoft Outlook 2013 solutions to find out if an attachment is considered unsafe and blocked for viewing and indexing.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe514-106">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="fe514-106">Interface identifier:</span></span>  <br/> |<span data-ttu-id="fe514-107">IID_IAttachmentSecurity</span><span class="sxs-lookup"><span data-stu-id="fe514-107">IID_IAttachmentSecurity</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="fe514-108">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="fe514-108">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="fe514-109">IAttachmentSecurity::IsAttachmentBlocked</span><span class="sxs-lookup"><span data-stu-id="fe514-109">IAttachmentSecurity::IsAttachmentBlocked</span></span>](iattachmentsecurity-isattachmentblocked.md) <br/> |<span data-ttu-id="fe514-110">Verifica se um anexo especificado é bloqueado pelo Outlook 2010 ou Outlook 2013 para exibição e indexação.</span><span class="sxs-lookup"><span data-stu-id="fe514-110">Checks if a specified attachment is blocked by Outlook 2010 or Outlook 2013 for viewing and indexing.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe514-111">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="fe514-111">Remarks</span></span>

<span data-ttu-id="fe514-112">Soluções do Outlook 2010 e o Outlook 2013 podem consultar a esta interface para ver se um anexo estiver bloqueado.</span><span class="sxs-lookup"><span data-stu-id="fe514-112">Outlook 2010 and Outlook 2013 solutions can query this interface to see if an attachment is blocked.</span></span> <span data-ttu-id="fe514-113">Os anexos que serão bloqueados pelo Outlook 2010 ou Outlook 2013 variam dependendo de como o Outlook 2010 ou Outlook 2013 foi configurado e as políticas que um administrador tiver sido aplicada.</span><span class="sxs-lookup"><span data-stu-id="fe514-113">The attachments that are blocked by Outlook 2010 or Outlook 2013 vary depending on how Outlook 2010 or Outlook 2013 has been configured and the policies that an administrator has applied.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe514-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe514-114">See also</span></span>



[<span data-ttu-id="fe514-115">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="fe514-115">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="fe514-116">Verifique se que um anexo estiver bloqueado</span><span class="sxs-lookup"><span data-stu-id="fe514-116">Verify an Attachment is Blocked</span></span>](how-to-verify-an-attachment-is-blocked.md)

