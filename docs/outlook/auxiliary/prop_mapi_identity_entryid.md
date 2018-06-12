---
title: PROP_MAPI_IDENTITY_ENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c64db8ea-d6ad-4fb9-97aa-958e5a0daf8f
description: Obtém ou define a identificação de entrada do catálogo de endereços para a conta.
ms.openlocfilehash: d85a779da36c2780fe058f906086f61cfc47d5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766060"
---
# <a name="propmapiidentityentryid"></a><span data-ttu-id="5160b-103">PROP_MAPI_IDENTITY_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="5160b-103">PROP_MAPI_IDENTITY_ENTRYID</span></span>

<span data-ttu-id="5160b-104">Obtém ou define a identificação de entrada do catálogo de endereços para a conta.</span><span class="sxs-lookup"><span data-stu-id="5160b-104">Retrieves or sets the address book entry ID for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5160b-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5160b-105">Quick info</span></span>

<span data-ttu-id="5160b-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="5160b-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5160b-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="5160b-107">Identifier:</span></span>  <br/> |<span data-ttu-id="5160b-108">0x2002</span><span class="sxs-lookup"><span data-stu-id="5160b-108">0x2002</span></span>  <br/> |
|<span data-ttu-id="5160b-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5160b-109">Property type:</span></span>  <br/> |<span data-ttu-id="5160b-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5160b-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5160b-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="5160b-111">Property tag:</span></span>  <br/> |<span data-ttu-id="5160b-112">0x20020102</span><span class="sxs-lookup"><span data-stu-id="5160b-112">0x20020102</span></span>  <br/> |
|<span data-ttu-id="5160b-113">Access:</span><span class="sxs-lookup"><span data-stu-id="5160b-113">Access:</span></span>  <br/> |<span data-ttu-id="5160b-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="5160b-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5160b-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="5160b-115">Remarks</span></span>

 <span data-ttu-id="5160b-116">**PROP\_MAPI\_identidade\_ENTRYID** não deve existir em cada conta.</span><span class="sxs-lookup"><span data-stu-id="5160b-116">**PROP\_MAPI\_IDENTITY\_ENTRYID** is not expected to exist on every account.</span></span> <span data-ttu-id="5160b-117">Por exemplo, uma conta do Exchange poderia ter **PROP\_MAPI\_identidade\_ENTRYID** definido e não [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md)enquanto revertida para uma conta de SMTP/POP3 a situação.</span><span class="sxs-lookup"><span data-stu-id="5160b-117">For example, an Exchange account could have **PROP\_MAPI\_IDENTITY\_ENTRYID** set and not [PROP\_ACCT_USER_EMAIL_ADDR](prop_acct_user_email_addr.md), while for an SMTP/POP3 account the situation is reversed.</span></span> <span data-ttu-id="5160b-118">**PROP\_MAPI_IDENTITY_ENTRYID** retorna uma identificação de entrada é semelhante ao valor retornado pela _lppEntryID_ em [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="5160b-118">**PROP\_MAPI_IDENTITY_ENTRYID** returns an entry ID that is similar to the value returned by  _lppEntryID_ in [IMAPISession::QueryIdentity](http://msdn.microsoft.com/library/a2cdda90-5457-49a7-b98c-7273ffe5cbbc%28Office.15%29.aspx).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5160b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="5160b-119">See also</span></span>

- [<span data-ttu-id="5160b-120">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="5160b-120">About the Account Management API</span></span>](about-the-account-management-api.md)

