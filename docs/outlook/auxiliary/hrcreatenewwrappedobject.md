---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Cria um objeto que um cliente pode acessar em um formato de caractere preferido.
ms.openlocfilehash: 3f68e0f275bcc5df065b3113d3322d6957f76df0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384189"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="2ddb6-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="2ddb6-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="2ddb6-104">Cria um objeto que um cliente pode acessar em um formato de caractere preferido.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2ddb6-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2ddb6-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2ddb6-106">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="2ddb6-106">Exported by:</span></span>  <br/> |<span data-ttu-id="2ddb6-107">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="2ddb6-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="2ddb6-108">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2ddb6-108">Called by:</span></span>  <br/> |<span data-ttu-id="2ddb6-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="2ddb6-109">Client</span></span>  <br/> |
|<span data-ttu-id="2ddb6-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2ddb6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="2ddb6-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="2ddb6-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="2ddb6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ddb6-112">Parameters</span></span>

<span data-ttu-id="2ddb6-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="2ddb6-114">[in] O objeto inicial não ajustado do Outlook.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="2ddb6-115">Deve implementar uma das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="2ddb6-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="2ddb6-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx) ou [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2ddb6-116">[IMailUser : IMAPIProp](https://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](https://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](https://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](https://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](https://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](https://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="2ddb6-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="2ddb6-118">[in] Sinalizadores que caracterizam o objeto inicial não ajustado.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="2ddb6-119">Deve ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2ddb6-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="2ddb6-120">DDLWRAP_FLAG_ANSI — O objeto não ajustado é ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="2ddb6-121">DDLWRAP_FLAG_UNICODE — O objeto não ajustado é UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="2ddb6-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="2ddb6-123">[in] Sinalizadores para o formato de caractere preferido.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="2ddb6-124">Deve ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2ddb6-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="2ddb6-125">DDLWRAP_FLAG_ANSI – O objeto ajustado será exposto como ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="2ddb6-126">DDLWRAP_FLAG_UNICODE– O objeto ajustado será exposto como UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="2ddb6-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-127">_pIID_</span></span>
  
>  <span data-ttu-id="2ddb6-128">[in] O identificador da interface com suporte pelo objeto não ajustado; defina como NULL se for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="2ddb6-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="2ddb6-130">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-130">[in] This parameter is not used.</span></span> <span data-ttu-id="2ddb6-131">Ele deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-131">It must be NULL.</span></span> 
    
<span data-ttu-id="2ddb6-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="2ddb6-133">[in] Defina este parâmetro como **true** se _pvUnwrapped_ deve ser verificado em relação a seu formato antes do ajuste; configure-o como **false** se o objeto deve ser ajustado sem verificação.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="2ddb6-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="2ddb6-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="2ddb6-135">[out] Um apontador para o objeto solicitado, ajustado no formato de caractere solicitado.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2ddb6-136">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="2ddb6-136">Return Values</span></span>

<span data-ttu-id="2ddb6-137">S_OK se a chamada for bem-sucedida; caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2ddb6-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ddb6-138">Remarks</span></span>

<span data-ttu-id="2ddb6-139">Passar um objeto ajustado com _fCheckWrap_ definido como **true** resultará em um objeto não ajustado.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="2ddb6-140">Independentemente de o objeto estar ajustado ou não, o cliente é responsável por liberar a referência no objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="2ddb6-141">Ao usar **GetProcAddress** para procurar o endereço dessa função em msmapi32.dll, especifique **HrCreateNewWrappedObject@28** como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="2ddb6-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ddb6-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ddb6-142">See also</span></span>

- [<span data-ttu-id="2ddb6-143">Sobre a API de camada de degradação de dados</span><span class="sxs-lookup"><span data-stu-id="2ddb6-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="2ddb6-144">Constantes (API de camada de degradação de dados)</span><span class="sxs-lookup"><span data-stu-id="2ddb6-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

