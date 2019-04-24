---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322152"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="4a0f8-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="4a0f8-102">IOlkAccountHelper</span></span>

<span data-ttu-id="4a0f8-103">Fornece funcionalidade de ajuda na sessão MAPI atual para gerenciar contas.</span><span class="sxs-lookup"><span data-stu-id="4a0f8-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4a0f8-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="4a0f8-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a0f8-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="4a0f8-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="4a0f8-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a0f8-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="4a0f8-107">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="4a0f8-107">Provided by:</span></span>  <br/> |<span data-ttu-id="4a0f8-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="4a0f8-108">Client</span></span>  <br/> |
|<span data-ttu-id="4a0f8-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="4a0f8-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4a0f8-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="4a0f8-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4a0f8-111">Vtable order</span><span class="sxs-lookup"><span data-stu-id="4a0f8-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4a0f8-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="4a0f8-112">Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="4a0f8-113">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="4a0f8-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="4a0f8-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="4a0f8-114">GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="4a0f8-115">Obtém o nome de um perfil de conta.</span><span class="sxs-lookup"><span data-stu-id="4a0f8-115">Gets the profile name of an account.</span></span>  <br/> |
|[<span data-ttu-id="4a0f8-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="4a0f8-116">GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="4a0f8-117">Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.</span><span class="sxs-lookup"><span data-stu-id="4a0f8-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="4a0f8-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="4a0f8-118">HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="4a0f8-119">Lança o objeto de sessão MAPI retornado por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="4a0f8-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a0f8-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a0f8-120">Remarks</span></span>

<span data-ttu-id="4a0f8-121">Essa interface é passada para [IOlkAccountManager::Init](iolkaccountmanager-init.md) ao inicializar o gerente de contas.</span><span class="sxs-lookup"><span data-stu-id="4a0f8-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a0f8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a0f8-122">See also</span></span>

- [<span data-ttu-id="4a0f8-123">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="4a0f8-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="4a0f8-124">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="4a0f8-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

