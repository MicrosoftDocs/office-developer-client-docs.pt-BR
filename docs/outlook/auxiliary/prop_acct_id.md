---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Retorna um identificador que identifica exclusivamente uma conta dentro do perfil no qual a conta é criada.
ms.openlocfilehash: dcb0a7935b9b764c44088971a1acb1f3647cbdb0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407162"
---
# <a name="propacctid"></a><span data-ttu-id="cda45-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="cda45-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="cda45-104">Retorna um identificador que identifica exclusivamente uma conta dentro do perfil no qual a conta é criada.</span><span class="sxs-lookup"><span data-stu-id="cda45-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cda45-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="cda45-105">Quick info</span></span>

<span data-ttu-id="cda45-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="cda45-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cda45-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cda45-107">Identifier:</span></span>  <br/> |<span data-ttu-id="cda45-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="cda45-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="cda45-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="cda45-109">Property type:</span></span>  <br/> |<span data-ttu-id="cda45-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cda45-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cda45-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="cda45-111">Property tag:</span></span>  <br/> |<span data-ttu-id="cda45-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="cda45-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="cda45-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="cda45-113">Access:</span></span>  <br/> |<span data-ttu-id="cda45-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cda45-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cda45-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cda45-115">Remarks</span></span>

<span data-ttu-id="cda45-116">Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="cda45-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="cda45-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="cda45-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="cda45-118">Essa propriedade é diferente de [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) , pois seu valor só é exclusivo entre todas as contas dentro desse perfil em que a conta foi criada, enquanto **prop\_ACCT_MINI_UID** identifica exclusivamente a conta dentro e fora do perfil no qual a conta foi criada.</span><span class="sxs-lookup"><span data-stu-id="cda45-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="cda45-119">Quando uma mensagem com essas propriedades é móvel para um segundo computador com um perfil do Outlook diferente e um conjunto diferente de contas, **PROP_ACCT_ID** pode entrar em conflito com uma conta no perfil do segundo computador e **PROP_ACCT_MINI_UID** pode identificar exclusivamente a conta original no perfil original.</span><span class="sxs-lookup"><span data-stu-id="cda45-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cda45-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="cda45-120">See also</span></span>

- [<span data-ttu-id="cda45-121">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="cda45-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="cda45-122">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="cda45-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

