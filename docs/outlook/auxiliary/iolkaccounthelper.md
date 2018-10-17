---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386408"
---
# <a name="iolkaccounthelper"></a><span data-ttu-id="6bbb6-102">IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="6bbb6-102">IOlkAccountHelper</span></span>

<span data-ttu-id="6bbb6-103">Fornece funcionalidade de ajuda na sessão MAPI atual para gerenciar contas.</span><span class="sxs-lookup"><span data-stu-id="6bbb6-103">Provides helper functionality in the current MAPI session to manage accounts.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6bbb6-104">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6bbb6-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6bbb6-105">Herda de:</span><span class="sxs-lookup"><span data-stu-id="6bbb6-105">Inherits from appleDeviceFeaturesConfigurationBase</span></span>  <br/> |[<span data-ttu-id="6bbb6-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bbb6-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="6bbb6-107">Fornecido por:</span><span class="sxs-lookup"><span data-stu-id="6bbb6-107">Provided by:</span></span>  <br/> |<span data-ttu-id="6bbb6-108">Cliente</span><span class="sxs-lookup"><span data-stu-id="6bbb6-108">Client</span></span>  <br/> |
|<span data-ttu-id="6bbb6-109">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="6bbb6-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6bbb6-110">IID_IOlkAccountHelper</span><span class="sxs-lookup"><span data-stu-id="6bbb6-110">IID_IOlkAccountHelper</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6bbb6-111">Vtable order</span><span class="sxs-lookup"><span data-stu-id="6bbb6-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6bbb6-112">Placeholder1</span><span class="sxs-lookup"><span data-stu-id="6bbb6-112">IFreeBusySupport::Placeholder1</span></span>](iolkaccounthelper-placeholder1.md) <br/> | <span data-ttu-id="6bbb6-113">*Esse membro é um espaço reservado e não tem suporte.*</span><span class="sxs-lookup"><span data-stu-id="6bbb6-113">*This member is a placeholder and is not supported.*</span></span>  <br/> |
|[<span data-ttu-id="6bbb6-114">GetIdentity</span><span class="sxs-lookup"><span data-stu-id="6bbb6-114">IOlkAccountHelper::GetIdentity</span></span>](iolkaccounthelper-getidentity.md) <br/> |<span data-ttu-id="6bbb6-115">Obtém o nome de um perfil de conta.</span><span class="sxs-lookup"><span data-stu-id="6bbb6-115">Gets the name of an account profile. Read/write  String.</span></span>  <br/> |
|[<span data-ttu-id="6bbb6-116">GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="6bbb6-116">IOlkAccountHelper::GetMapiSession</span></span>](iolkaccounthelper-getmapisession.md) <br/> |<span data-ttu-id="6bbb6-117">Abre uma sessão MAPI e mantém uma referência à sessão para o gerente de conta.</span><span class="sxs-lookup"><span data-stu-id="6bbb6-117">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>  <br/> |
|[<span data-ttu-id="6bbb6-118">HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="6bbb6-118">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md) <br/> |<span data-ttu-id="6bbb6-119">Lança o objeto de sessão MAPI retornado por [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span><span class="sxs-lookup"><span data-stu-id="6bbb6-119">Releases the MAPI session object that was returned by [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bbb6-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6bbb6-120">Remarks</span></span>

<span data-ttu-id="6bbb6-121">Essa interface é passada para [IOlkAccountManager::Init](iolkaccountmanager-init.md) ao inicializar o gerente de contas.</span><span class="sxs-lookup"><span data-stu-id="6bbb6-121">This interface is passed to [IOlkAccountManager::Init](iolkaccountmanager-init.md) when initializing the account manager.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6bbb6-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="6bbb6-122">See also</span></span>

- [<span data-ttu-id="6bbb6-123">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="6bbb6-123">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="6bbb6-124">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="6bbb6-124">Constants (Account management API)</span></span>](constants-account-management-api.md)

