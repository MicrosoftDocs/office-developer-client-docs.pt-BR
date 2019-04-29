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
# <a name="propacctuseremailaddr"></a><span data-ttu-id="8ba7e-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="8ba7e-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="8ba7e-104">Especifica o endereço de email da conta.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8ba7e-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8ba7e-105">Quick info</span></span>

<span data-ttu-id="8ba7e-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8ba7e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8ba7e-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8ba7e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="8ba7e-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="8ba7e-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="8ba7e-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="8ba7e-109">Property type:</span></span>  <br/> |<span data-ttu-id="8ba7e-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8ba7e-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8ba7e-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="8ba7e-111">Property tag:</span></span>  <br/> |<span data-ttu-id="8ba7e-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="8ba7e-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="8ba7e-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="8ba7e-113">Access:</span></span>  <br/> |<span data-ttu-id="8ba7e-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8ba7e-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8ba7e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ba7e-115">Remarks</span></span>

 <span data-ttu-id="8ba7e-116">**PROP_ACCT_USER_EMAIL_ADDR** não deve existir em todas as contas.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="8ba7e-117">Por exemplo, uma conta do Exchange poderia ter [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) mas não **PROP_ACCT_USER_EMAIL_ADDR**, enquanto for uma conta SMTP/POP3, a situação será revertida.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8ba7e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ba7e-118">See also</span></span>

- [<span data-ttu-id="8ba7e-119">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="8ba7e-119">About the Account Management API</span></span>](about-the-account-management-api.md)

