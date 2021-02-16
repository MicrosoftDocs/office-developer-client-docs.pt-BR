---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica o endereço de email da conta.
ms.openlocfilehash: 115941fdf2fdec01da8d6bc1320ac6cdc0930ffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436773"
---
# <a name="prop_acct_user_email_addr"></a><span data-ttu-id="a5265-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="a5265-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="a5265-104">Especifica o endereço de email da conta.</span><span class="sxs-lookup"><span data-stu-id="a5265-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a5265-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a5265-105">Quick info</span></span>

<span data-ttu-id="a5265-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a5265-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a5265-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a5265-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a5265-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="a5265-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="a5265-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a5265-109">Property type:</span></span>  <br/> |<span data-ttu-id="a5265-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5265-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a5265-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a5265-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a5265-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="a5265-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="a5265-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="a5265-113">Access:</span></span>  <br/> |<span data-ttu-id="a5265-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="a5265-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a5265-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5265-115">Remarks</span></span>

 <span data-ttu-id="a5265-116">**PROP_ACCT_USER_EMAIL_ADDR** se espera que exista em todas as contas.</span><span class="sxs-lookup"><span data-stu-id="a5265-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="a5265-117">Por exemplo, uma conta [](prop_mapi_identity_entryid.md) do Exchange pode ter PROP_MAPI_IDENTITY_ENTRYID, mas não **PROP_ACCT_USER_EMAIL_ADDR**, enquanto para uma conta SMTP/POP3, a situação é invertida.</span><span class="sxs-lookup"><span data-stu-id="a5265-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a5265-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5265-118">See also</span></span>

- [<span data-ttu-id="a5265-119">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="a5265-119">About the Account Management API</span></span>](about-the-account-management-api.md)

