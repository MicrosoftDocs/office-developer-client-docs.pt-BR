---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True se a conta for uma conta do Exchange.
ms.openlocfilehash: 2df750b208ff9d2a18cb0d7c22ec6b32b658c7b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327647"
---
# <a name="propacctisexch"></a><span data-ttu-id="4ba25-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="4ba25-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="4ba25-104">True se a conta for uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="4ba25-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4ba25-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4ba25-105">Quick info</span></span>

<span data-ttu-id="4ba25-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="4ba25-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4ba25-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4ba25-107">Identifier:</span></span>  <br/> |<span data-ttu-id="4ba25-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="4ba25-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="4ba25-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="4ba25-109">Property type:</span></span>  <br/> |<span data-ttu-id="4ba25-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="4ba25-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="4ba25-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="4ba25-111">Property tag:</span></span>  <br/> |<span data-ttu-id="4ba25-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="4ba25-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="4ba25-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="4ba25-113">Access:</span></span>  <br/> |<span data-ttu-id="4ba25-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="4ba25-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ba25-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4ba25-115">Remarks</span></span>

<span data-ttu-id="4ba25-116">Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="4ba25-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="4ba25-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="4ba25-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4ba25-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="4ba25-118">See also</span></span>

- [<span data-ttu-id="4ba25-119">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="4ba25-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="4ba25-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="4ba25-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

