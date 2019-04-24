---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: 59f43e8b3b0819b0178d60fa357e01937ae19d81
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322096"
---
# <a name="iolkenum"></a><span data-ttu-id="f70f2-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="f70f2-102">IOlkEnum</span></span>

<span data-ttu-id="f70f2-103">Oferece suporte à enumeração de contas como objetos [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f70f2-103">Supports enumerating accounts as [IUnknown](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="f70f2-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="f70f2-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f70f2-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="f70f2-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="f70f2-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="f70f2-106">IUnknown</span></span>](https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="f70f2-107">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f70f2-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="f70f2-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="f70f2-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="f70f2-109">Provided by:</span><span class="sxs-lookup"><span data-stu-id="f70f2-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="f70f2-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="f70f2-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="f70f2-111">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f70f2-111">Called by:</span></span>  <br/> |<span data-ttu-id="f70f2-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="f70f2-112">Client</span></span>  <br/> |
|<span data-ttu-id="f70f2-113">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="f70f2-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f70f2-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="f70f2-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f70f2-115">Vtable order</span><span class="sxs-lookup"><span data-stu-id="f70f2-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f70f2-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="f70f2-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="f70f2-117">Obtém o número de contas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="f70f2-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="f70f2-118">Reset</span><span class="sxs-lookup"><span data-stu-id="f70f2-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="f70f2-119">Redefine o enumerador para o início.</span><span class="sxs-lookup"><span data-stu-id="f70f2-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="f70f2-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="f70f2-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="f70f2-121">Obtém a próxima conta no enumerador.</span><span class="sxs-lookup"><span data-stu-id="f70f2-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="f70f2-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="f70f2-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="f70f2-123">Ignora um número especificado de contas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="f70f2-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f70f2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f70f2-124">Remarks</span></span>

<span data-ttu-id="f70f2-125">Essa interface é retornada por **IOlkAccountManager:: EnumerateAccounts** ao obter um enumerador de contas.</span><span class="sxs-lookup"><span data-stu-id="f70f2-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f70f2-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="f70f2-126">See also</span></span>

- [<span data-ttu-id="f70f2-127">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="f70f2-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="f70f2-128">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="f70f2-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

