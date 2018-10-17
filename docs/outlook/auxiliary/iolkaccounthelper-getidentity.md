---
title: IOlkAccountHelperGetIdentity
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea8b8f02-959f-cd71-9cfe-5ebdf4bae2bc
description: Obtém o nome de um perfil de conta.
ms.openlocfilehash: d725f309a29b026395e2795a49d31b45a4a49562
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400135"
---
# <a name="iolkaccounthelpergetidentity"></a><span data-ttu-id="29f31-103">IOlkAccountHelper::GetIdentity</span><span class="sxs-lookup"><span data-stu-id="29f31-103">IOlkAccountHelper::GetIdentity</span></span>

<span data-ttu-id="29f31-104">Obtém o nome de um perfil de conta.</span><span class="sxs-lookup"><span data-stu-id="29f31-104">Gets the name of an account profile. Read/write  String.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="29f31-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="29f31-105">Quick info</span></span>

<span data-ttu-id="29f31-106">Confira [IOlkAccountHelper](iolkaccounthelper.md).</span><span class="sxs-lookup"><span data-stu-id="29f31-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetIdentity (  
    LPWSTR pwszIdentity, 
    DWORD *pcch 
);
```

## <a name="parameters"></a><span data-ttu-id="29f31-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29f31-107">Parameters</span></span>

<span data-ttu-id="29f31-108">_pwszIdentity_</span><span class="sxs-lookup"><span data-stu-id="29f31-108">_pwszIdentity_</span></span>
  
> <span data-ttu-id="29f31-109">[in][out] O nome do perfil.</span><span class="sxs-lookup"><span data-stu-id="29f31-109">[in][out] The profile name.</span></span>
    
<span data-ttu-id="29f31-110">_pcch_</span><span class="sxs-lookup"><span data-stu-id="29f31-110">_pcch_</span></span>
  
> <span data-ttu-id="29f31-111">[in] [out] Na chamada desse método, contém o tamanho (em número de caracteres) de _pwszIdentity_ que foi alocada.</span><span class="sxs-lookup"><span data-stu-id="29f31-111">[in] [out] Upon calling this method, contains the size (in number of characters) of  _pwszIdentity_ that has been allocated.</span></span> <span data-ttu-id="29f31-112">No retorno, contém o tamanho real, incluindo o caractere 0 de encerramento, do nome de perfil retornado.</span><span class="sxs-lookup"><span data-stu-id="29f31-112">Upon return, contains the actual length, including the 0-terminating character, of the returned profile name.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="29f31-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="29f31-113">Return Values</span></span>

|<span data-ttu-id="29f31-114">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="29f31-114">**HRESULT**</span></span>|<span data-ttu-id="29f31-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29f31-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29f31-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="29f31-116">S_OK</span></span>  <br/> |<span data-ttu-id="29f31-117">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="29f31-117">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="29f31-118">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="29f31-118">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="29f31-119">O nome de perfil retornado é maior do que _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="29f31-119">The returned profile name is longer than the size of  _pwszIdentity_.</span></span>  <br/> |
|<span data-ttu-id="29f31-120">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="29f31-120">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="29f31-121">_pcch_ é NULL.</span><span class="sxs-lookup"><span data-stu-id="29f31-121">_pcch_ is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29f31-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="29f31-122">Remarks</span></span>

<span data-ttu-id="29f31-123">Se _pwszIdentity_ for muito pequeno para armazenar o nome de perfil, ele não será definido no retorno, e _pcch_ apontará para o tamanho obrigatório para _pwszIdentity_.</span><span class="sxs-lookup"><span data-stu-id="29f31-123">If  _pwszIdentity_ is too small to hold the profile name, it will not be set on return, and  _pcch_ will point to the size required for  _pwszIdentity_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="29f31-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="29f31-124">See also</span></span>

- [<span data-ttu-id="29f31-125">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="29f31-125">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="29f31-126">PidTagProfileName</span><span class="sxs-lookup"><span data-stu-id="29f31-126">PidTagProfileName</span></span>](https://msdn.microsoft.com/library/13ca726d-ae7a-4da9-9c8e-3db3c479f839%28Office.15%29.aspx)

