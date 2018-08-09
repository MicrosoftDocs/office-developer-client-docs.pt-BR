---
title: PROP_ACCT_USER_EMAIL_ADDR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fe447899-d37a-4775-a09d-13ba3a878008
description: Especifica o endereço de email para a conta.
ms.openlocfilehash: 7d0bbba2dcb104326c360da6a10f3e19d1740e46
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766063"
---
# <a name="propacctuseremailaddr"></a><span data-ttu-id="30a7d-103">PROP_ACCT_USER_EMAIL_ADDR</span><span class="sxs-lookup"><span data-stu-id="30a7d-103">PROP_ACCT_USER_EMAIL_ADDR</span></span>

<span data-ttu-id="30a7d-104">Especifica o endereço de email para a conta.</span><span class="sxs-lookup"><span data-stu-id="30a7d-104">Specifies the email address for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30a7d-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="30a7d-105">Quick info</span></span>

<span data-ttu-id="30a7d-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="30a7d-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="30a7d-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="30a7d-107">Identifier:</span></span>  <br/> |<span data-ttu-id="30a7d-108">0x000C</span><span class="sxs-lookup"><span data-stu-id="30a7d-108">0x000C</span></span>  <br/> |
|<span data-ttu-id="30a7d-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="30a7d-109">Property type:</span></span>  <br/> |<span data-ttu-id="30a7d-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="30a7d-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="30a7d-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="30a7d-111">Property tag:</span></span>  <br/> |<span data-ttu-id="30a7d-112">0x000C001F</span><span class="sxs-lookup"><span data-stu-id="30a7d-112">0x000C001F</span></span>  <br/> |
|<span data-ttu-id="30a7d-113">Access:</span><span class="sxs-lookup"><span data-stu-id="30a7d-113">Access:</span></span>  <br/> |<span data-ttu-id="30a7d-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="30a7d-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="30a7d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="30a7d-115">Remarks</span></span>

 <span data-ttu-id="30a7d-116">Espera- **PROP_ACCT_USER_EMAIL_ADDR** não existir em cada conta.</span><span class="sxs-lookup"><span data-stu-id="30a7d-116">**PROP_ACCT_USER_EMAIL_ADDR** is not expected to exist on every account.</span></span> <span data-ttu-id="30a7d-117">Por exemplo, uma conta do Exchange poderia ter [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) , mas não **PROP_ACCT_USER_EMAIL_ADDR**, enquanto que para uma conta de SMTP/POP3, a situação é inversa.</span><span class="sxs-lookup"><span data-stu-id="30a7d-117">For example, an Exchange account could have [PROP_MAPI_IDENTITY_ENTRYID](prop_mapi_identity_entryid.md) but not **PROP_ACCT_USER_EMAIL_ADDR**, while for an SMTP/POP3 account, the situation is reversed.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30a7d-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="30a7d-118">See also</span></span>

- [<span data-ttu-id="30a7d-119">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="30a7d-119">About the Account Management API</span></span>](about-the-account-management-api.md)

