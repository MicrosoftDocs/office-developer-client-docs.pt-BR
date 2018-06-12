---
title: IOlkEnum
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 33cb89cb-c967-760c-6bc4-94118a4f872c
ms.openlocfilehash: be91a56f93b787f5570139768d96eb4f7fe9ac02
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765995"
---
# <a name="iolkenum"></a><span data-ttu-id="5b290-102">IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="5b290-102">IOlkEnum</span></span>

<span data-ttu-id="5b290-103">Suporta enumerando contas como objetos [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5b290-103">Supports enumerating accounts as [IUnknown](http://msdn.microsoft.com/library/com.iunknown%28Office.15%29.aspx) objects.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="5b290-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="5b290-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5b290-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="5b290-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="5b290-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b290-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="5b290-107">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="5b290-107">Implemented by:</span></span>  <br/> |<span data-ttu-id="5b290-108">Outlook</span><span class="sxs-lookup"><span data-stu-id="5b290-108">Outlook</span></span>  <br/> |
|<span data-ttu-id="5b290-109">Provided by:</span><span class="sxs-lookup"><span data-stu-id="5b290-109">Provided by:</span></span>  <br/> |[<span data-ttu-id="5b290-110">IOlkAccountManager::EnumerateAccounts</span><span class="sxs-lookup"><span data-stu-id="5b290-110">IOlkAccountManager::EnumerateAccounts</span></span>](iolkaccountmanager-enumerateaccounts.md) <br/> |
|<span data-ttu-id="5b290-111">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="5b290-111">Called by:</span></span>  <br/> |<span data-ttu-id="5b290-112">Cliente</span><span class="sxs-lookup"><span data-stu-id="5b290-112">Client</span></span>  <br/> |
|<span data-ttu-id="5b290-113">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="5b290-113">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5b290-114">IID_IOlkEnum</span><span class="sxs-lookup"><span data-stu-id="5b290-114">IID_IOlkEnum</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5b290-115">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="5b290-115">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5b290-116">GetCount</span><span class="sxs-lookup"><span data-stu-id="5b290-116">GetCount</span></span>](iolkenum-getcount.md) <br/> |<span data-ttu-id="5b290-117">Obtém o número de contas no enumerador.</span><span class="sxs-lookup"><span data-stu-id="5b290-117">Gets the number of accounts in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="5b290-118">Reset</span><span class="sxs-lookup"><span data-stu-id="5b290-118">Reset</span></span>](iolkenum-reset.md) <br/> |<span data-ttu-id="5b290-119">Redefine o enumerador para o início.</span><span class="sxs-lookup"><span data-stu-id="5b290-119">Resets the enumerator to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="5b290-120">GetNext</span><span class="sxs-lookup"><span data-stu-id="5b290-120">GetNext</span></span>](iolkenum-getnext.md) <br/> |<span data-ttu-id="5b290-121">Obtém a próxima conta no enumerador.</span><span class="sxs-lookup"><span data-stu-id="5b290-121">Gets the next account in the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="5b290-122">Ignorar</span><span class="sxs-lookup"><span data-stu-id="5b290-122">Skip</span></span>](iolkenum-skip.md) <br/> |<span data-ttu-id="5b290-123">Ignora um número especificado de contas do enumerador.</span><span class="sxs-lookup"><span data-stu-id="5b290-123">Skips a specified number of accounts in the enumerator.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b290-124">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="5b290-124">Remarks</span></span>

<span data-ttu-id="5b290-125">Esta interface é retornado por **IOlkAccountManager::EnumerateAccounts** ao obter um enumerador de contas.</span><span class="sxs-lookup"><span data-stu-id="5b290-125">This interface is returned by **IOlkAccountManager::EnumerateAccounts** when obtaining an enumerator of accounts.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5b290-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5b290-126">See also</span></span>

- [<span data-ttu-id="5b290-127">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="5b290-127">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="5b290-128">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="5b290-128">Constants (Account management API)</span></span>](constants-account-management-api.md)

