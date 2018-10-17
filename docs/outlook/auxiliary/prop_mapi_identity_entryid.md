---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Recupera ou define a ID de entrada do catálogo de endereços da conta.
ms.openlocfilehash: 2352f64b46e9884e95b7bf1f3693321f7cd224ca
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400342"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="5d36e-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5d36e-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="5d36e-104">Recupera ou define a ID de entrada do catálogo de endereços da conta.</span><span class="sxs-lookup"><span data-stu-id="5d36e-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5d36e-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5d36e-105">Quick info</span></span>

<span data-ttu-id="5d36e-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="5d36e-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5d36e-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5d36e-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5d36e-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="5d36e-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="5d36e-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5d36e-109">Property type</span></span>  <br/> |<span data-ttu-id="5d36e-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5d36e-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5d36e-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5d36e-111">Property Tag</span></span>  <br/> |<span data-ttu-id="5d36e-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="5d36e-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="5d36e-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="5d36e-113">Access</span></span>  <br/> |<span data-ttu-id="5d36e-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5d36e-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d36e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d36e-115">Remarks</span></span>

 <span data-ttu-id="5d36e-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** não precisa existir em toda conta.</span><span class="sxs-lookup"><span data-stu-id="5d36e-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="5d36e-117">Por exemplo, uma conta do Exchange pode ter **PROP\_MAPI\_IDENTITY\_ENTRYID** definidos, e não [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), enquanto para uma conta POP3/SMTP a situação é reversa.</span><span class="sxs-lookup"><span data-stu-id="5d36e-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="5d36e-118">**PROP\_MAPI_IDENTITY_ENTRYID** retorna uma ID de entrada semelhante ao valor retornado por _lppEntryID_ em [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5d36e-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](https://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d36e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d36e-119">See also</span></span>

- [<span data-ttu-id="5d36e-120">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="5d36e-120">About the Account Management API</span></span>](about-the-account-management-api.md)

