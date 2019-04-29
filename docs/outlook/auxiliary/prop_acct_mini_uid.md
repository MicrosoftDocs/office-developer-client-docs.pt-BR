---
title: PROP_ACCT_MINI_UID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 30d8268e-0c64-401d-8799-e8e1ba78b88f
description: Retorna um identificador de conta exclusivo nos perfis do Outlook.
ms.openlocfilehash: 209f7dd89b8d947b999f2a068373aaf61a3e9784
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409430"
---
# <a name="propacctminiuid"></a><span data-ttu-id="d11bf-103">PROP_ACCT_MINI_UID</span><span class="sxs-lookup"><span data-stu-id="d11bf-103">PROP_ACCT_MINI_UID</span></span>

<span data-ttu-id="d11bf-104">Retorna um identificador de conta exclusivo nos perfis do Outlook.</span><span class="sxs-lookup"><span data-stu-id="d11bf-104">Returns an account identifier that is unique across Outlook profiles.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d11bf-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d11bf-105">Quick info</span></span>

<span data-ttu-id="d11bf-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d11bf-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d11bf-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d11bf-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d11bf-108">0x0003</span><span class="sxs-lookup"><span data-stu-id="d11bf-108">0x0003</span></span>  <br/> |
|<span data-ttu-id="d11bf-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d11bf-109">Property type:</span></span>  <br/> |<span data-ttu-id="d11bf-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="d11bf-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="d11bf-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d11bf-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d11bf-112">0x00030003</span><span class="sxs-lookup"><span data-stu-id="d11bf-112">0x00030003</span></span>  <br/> |
|<span data-ttu-id="d11bf-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="d11bf-113">Access:</span></span>  <br/> |<span data-ttu-id="d11bf-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d11bf-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d11bf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d11bf-115">Remarks</span></span>

<span data-ttu-id="d11bf-116">Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="d11bf-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="d11bf-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="d11bf-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="d11bf-118">Essa propriedade é diferente de [PROP_ACCT_ID](prop_acct_id.md) , pois seu valor identifica exclusivamente a conta dentro e fora do perfil no qual a conta foi criada, enquanto **PROP_ACCT_ID** é exclusiva somente entre todas as contas dentro de um perfil em que a conta foi criada.</span><span class="sxs-lookup"><span data-stu-id="d11bf-118">This property is different from [PROP_ACCT_ID](prop_acct_id.md) in that its value uniquely identifies the account within and outside of the profile in which the account was created, whereas **PROP_ACCT_ID** is unique only among all the accounts within that one profile in which the account was created.</span></span> <span data-ttu-id="d11bf-119">Quando uma mensagem com essas propriedades é móvel para um segundo computador com um perfil do Outlook diferente e um conjunto diferente de contas, o **PROP_ACCT_MINI_UID** pode identificar exclusivamente a conta original no perfil original.</span><span class="sxs-lookup"><span data-stu-id="d11bf-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> <span data-ttu-id="d11bf-120">No enTanto, **PROP_ACCT_ID** pode possivelmente entrar em conflito com uma conta no perfil do segundo computador.</span><span class="sxs-lookup"><span data-stu-id="d11bf-120">However, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d11bf-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d11bf-121">See also</span></span>

- [<span data-ttu-id="d11bf-122">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="d11bf-122">PROP_ACCT_ID</span></span>](prop_acct_id.md)  
- [<span data-ttu-id="d11bf-123">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="d11bf-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="d11bf-124">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="d11bf-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

