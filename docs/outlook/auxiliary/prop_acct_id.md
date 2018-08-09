---
title: PROP_ACCT_ID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b72124aa-2e85-057c-9343-a40af60b91a0
description: Retorna um identificador que identifica exclusivamente uma conta dentro do perfil na qual a conta é criada.
ms.openlocfilehash: a4ae193b89132ea718e16aec82f592205f9771c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766058"
---
# <a name="propacctid"></a><span data-ttu-id="c72d4-103">PROP_ACCT_ID</span><span class="sxs-lookup"><span data-stu-id="c72d4-103">PROP_ACCT_ID</span></span>

<span data-ttu-id="c72d4-104">Retorna um identificador que identifica exclusivamente uma conta dentro do perfil na qual a conta é criada.</span><span class="sxs-lookup"><span data-stu-id="c72d4-104">Returns an identifier that uniquely identifies an account within the profile in which the account is created.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c72d4-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="c72d4-105">Quick info</span></span>

<span data-ttu-id="c72d4-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="c72d4-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c72d4-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c72d4-107">Identifier:</span></span>  <br/> |<span data-ttu-id="c72d4-108">0x0001</span><span class="sxs-lookup"><span data-stu-id="c72d4-108">0x0001</span></span>  <br/> |
|<span data-ttu-id="c72d4-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="c72d4-109">Property type:</span></span>  <br/> |<span data-ttu-id="c72d4-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c72d4-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c72d4-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="c72d4-111">Property tag:</span></span>  <br/> |<span data-ttu-id="c72d4-112">0x00010003</span><span class="sxs-lookup"><span data-stu-id="c72d4-112">0x00010003</span></span>  <br/> |
|<span data-ttu-id="c72d4-113">Access:</span><span class="sxs-lookup"><span data-stu-id="c72d4-113">Access:</span></span>  <br/> |<span data-ttu-id="c72d4-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c72d4-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c72d4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c72d4-115">Remarks</span></span>

<span data-ttu-id="c72d4-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="c72d4-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="c72d4-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="c72d4-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
<span data-ttu-id="c72d4-118">Essa propriedade é diferente do [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) seu valor é exclusivo somente entre todas as contas dentro desse perfil no qual a conta foi criada, enquanto **PROP\_ACCT_MINI_UID** identifica exclusivamente a conta dentro e fora do perfil no qual a conta foi criada.</span><span class="sxs-lookup"><span data-stu-id="c72d4-118">This property is different from [PROP_ACCT_MINI_UID](prop_acct_mini_uid.md) in that its value is unique only among all the accounts within that profile in which the account was created, whereas **PROP\_ACCT_MINI_UID** uniquely identifies the account within and outside of the profile in which the account was created.</span></span> <span data-ttu-id="c72d4-119">Quando uma mensagem com essas propriedades se movimenta em um segundo computador com um perfil diferente do Outlook e um conjunto diferente de contas, **PROP_ACCT_ID** possivelmente pode entrar em conflito com uma conta no perfil do segundo computador e **PROP_ACCT_MINI_UID** podem identificar exclusivamente a conta original no perfil original.</span><span class="sxs-lookup"><span data-stu-id="c72d4-119">When a message with these properties roams onto a second computer with a different Outlook profile and different set of accounts, **PROP_ACCT_ID** can possibly conflict with an account in the profile of the second computer, and **PROP_ACCT_MINI_UID** can uniquely identify the original account in the original profile.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c72d4-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="c72d4-120">See also</span></span>

- [<span data-ttu-id="c72d4-121">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="c72d4-121">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="c72d4-122">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="c72d4-122">Constants (Account management API)</span></span>](constants-account-management-api.md)

