---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Retorna um identificador de conta que seja exclusivo entre perfis do Outlook.
ms.openlocfilehash: 9b2e30c0f57a54af219e68a8c2fe91e5dba4ddbe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766059"
---
# <a name="propacctminiuid"></a><span data-ttu-id="ab7b2-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="ab7b2-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="ab7b2-104">Retorna um identificador de conta que seja exclusivo entre perfis do Outlook.</span><span class="sxs-lookup"><span data-stu-id="ab7b2-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ab7b2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ab7b2-105">Quick info</span></span>

<span data-ttu-id="ab7b2-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="ab7b2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ab7b2-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ab7b2-107">Identifier:</span></span>  <br/> |<span data-ttu-id="ab7b2-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="ab7b2-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="ab7b2-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="ab7b2-109">Property type:</span></span>  <br/> |<span data-ttu-id="ab7b2-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="ab7b2-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="ab7b2-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="ab7b2-111">Property tag:</span></span>  <br/> |<span data-ttu-id="ab7b2-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="ab7b2-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="ab7b2-113">Access:</span><span class="sxs-lookup"><span data-stu-id="ab7b2-113">Access:</span></span>  <br/> |<span data-ttu-id="ab7b2-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab7b2-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab7b2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab7b2-115">Remarks</span></span>

<span data-ttu-id="ab7b2-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="ab7b2-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="ab7b2-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="ab7b2-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="ab7b2-118">Essa propriedade é diferente do [PROP_ACCT_ID](prop_acct_id.md) em que seu valor identifica exclusivamente a conta dentro e fora do perfil no qual a conta foi criada, enquanto **PROP_ACCT_ID** é exclusiva somente entre todas as contas em que um único perfil em que a conta foi criada.</span><span class="sxs-lookup"><span data-stu-id="ab7b2-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="ab7b2-119">Quando uma mensagem com essas propriedades se movimenta em um segundo computador com um perfil diferente do Outlook e um conjunto diferente de contas, **PROP_ACCT_MINI_UID** podem identificar exclusivamente a conta original no perfil original.</span><span class="sxs-lookup"><span data-stu-id="ab7b2-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="ab7b2-120">No entanto, **PROP_ACCT_ID** possivelmente podem entrar em conflito com uma conta no perfil do segundo computador.</span><span class="sxs-lookup"><span data-stu-id="ab7b2-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab7b2-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab7b2-121">See also</span></span>

- [<span data-ttu-id="ab7b2-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="ab7b2-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="ab7b2-123">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="ab7b2-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="ab7b2-124">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="ab7b2-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

