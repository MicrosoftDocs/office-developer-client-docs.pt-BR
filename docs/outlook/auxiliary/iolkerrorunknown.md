---
title: IOlkErrorUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9cfbf12c-a71c-092b-d86a-c5585b0f1edb
ms.openlocfilehash: 311d055e0a319ec26cdc4eba5ac3b50dc9e63d9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565176"
---
# <a name="iolkerrorunknown"></a><span data-ttu-id="a7759-102">IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="a7759-102">IOlkErrorUnknown</span></span>

<span data-ttu-id="a7759-103">Fornece informações adicionais sobre o último erro.</span><span class="sxs-lookup"><span data-stu-id="a7759-103">Provides extra information about the last error.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a7759-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a7759-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a7759-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="a7759-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="a7759-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7759-106">IUnknown</span></span>](https://docs.microsoft.com/en-us/windows/desktop/api/unknwn/nn-unknwn-iunknown) <br/> |
|<span data-ttu-id="a7759-107">Provided by:</span><span class="sxs-lookup"><span data-stu-id="a7759-107">Provided by:</span></span>  <br/> |<span data-ttu-id="a7759-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="a7759-108">Client</span></span>  <br/> |
|<span data-ttu-id="a7759-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a7759-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a7759-110">IID_IOlkErrorUnknown</span><span class="sxs-lookup"><span data-stu-id="a7759-110">IID_IOlkErrorUnknown</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a7759-111">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="a7759-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a7759-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a7759-112">GetLastError</span></span>](iolkerrorunknown-getlasterror.md) <br/> |<span data-ttu-id="a7759-113">Obtém uma cadeia de caracteres da mensagem de erro especificado.</span><span class="sxs-lookup"><span data-stu-id="a7759-113">Gets a message string for the specified error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7759-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7759-114">Remarks</span></span>

<span data-ttu-id="a7759-115">Essa interface fornece informações adicionais sobre um erro em [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md)e [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a7759-115">This interface provides extra information about an error in [IOlkAccountManager](iolkaccountmanager.md), [IOlkAccountNotify](iolkaccountnotify.md), and [IOlkAccount](iolkaccount.md).</span></span> <span data-ttu-id="a7759-116">Também é a interface de base para **IOlkAccountManager**, **IOlkAccountNotify**e **IOlkAccount**.</span><span class="sxs-lookup"><span data-stu-id="a7759-116">It is also the base interface for **IOlkAccountManager**, **IOlkAccountNotify**, and **IOlkAccount**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7759-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7759-117">See also</span></span>

- [<span data-ttu-id="a7759-118">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="a7759-118">About the Account Management API</span></span>](about-the-account-management-api.md)

