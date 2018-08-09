---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtém o nome do perfil de uma conta.
ms.openlocfilehash: 81417282faa9ba0e7ec99990ac78045b54752acb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765960"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="6d199-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="6d199-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="6d199-104">Obtém o nome do perfil de uma conta.</span><span class="sxs-lookup"><span data-stu-id="6d199-104">Gets the profile name of an account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6d199-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="6d199-105">Quick info</span></span>

<span data-ttu-id="6d199-106">Consulte [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="6d199-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="6d199-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d199-107">Parameters</span></span>

<span data-ttu-id="6d199-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="6d199-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="6d199-109">[in] [out] O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="6d199-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="6d199-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="6d199-110">_pcch_</span></span>
  
> <span data-ttu-id="6d199-111">[in] [out] Após chamar este método, contém o tamanho (em número de caracteres) da _pwszIdentity_ que foi alocado.</span><span class="sxs-lookup"><span data-stu-id="6d199-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="6d199-112">Após retornar, contém o tamanho real, incluindo o caractere de terminação de 0, o nome do perfil retornado.</span><span class="sxs-lookup"><span data-stu-id="6d199-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="6d199-113">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="6d199-113">Return values</span></span>

|<span data-ttu-id="6d199-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6d199-114">**HRESULT**</span></span>|<span data-ttu-id="6d199-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6d199-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6d199-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d199-116">S_OK</span></span>  <br/> |<span data-ttu-id="6d199-117">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6d199-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="6d199-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="6d199-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="6d199-119">O nome do perfil retornado é maior que o tamanho da _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="6d199-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="6d199-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="6d199-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="6d199-121">_pcch_ é nulo.</span><span class="sxs-lookup"><span data-stu-id="6d199-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d199-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d199-122">Remarks</span></span>

<span data-ttu-id="6d199-123">Se _pwszIdentity_ for muito pequeno para conter o nome do perfil, ela não será definida no retorno e _pcch_ irá apontar para o tamanho necessário para _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="6d199-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6d199-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d199-124">See also</span></span>

- [<span data-ttu-id="6d199-125">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="6d199-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="6d199-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="6d199-126">PidTagProfileName</span></span>](http://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

