---
title: IMAPIPropGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.GetLastError
api_type:
- COM
ms.assetid: f64a765d-c653-4eef-a0fc-24a54968757c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8c31cbf0472d3d64c7327fcfc80480ef27a1638e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342046"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="2cd57-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="2cd57-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="2cd57-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2cd57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2cd57-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior.</span><span class="sxs-lookup"><span data-stu-id="2cd57-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="2cd57-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2cd57-106">Parameters</span></span>

 <span data-ttu-id="2cd57-107">_And_</span><span class="sxs-lookup"><span data-stu-id="2cd57-107">_hResult_</span></span>
  
> <span data-ttu-id="2cd57-108">no Um identificador para o código de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="2cd57-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="2cd57-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2cd57-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2cd57-110">no Uma bitmask de sinalizadores que indica o formato do texto retornado na estrutura **MAPIERROR** indicada por _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="2cd57-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="2cd57-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="2cd57-111">The following flag can be set:</span></span>
    
<span data-ttu-id="2cd57-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2cd57-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2cd57-113">As cadeias de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2cd57-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="2cd57-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2cd57-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="2cd57-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="2cd57-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="2cd57-116">bota Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="2cd57-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="2cd57-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver informações de erro a serem retornadas.</span><span class="sxs-lookup"><span data-stu-id="2cd57-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2cd57-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2cd57-118">Return value</span></span>

<span data-ttu-id="2cd57-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="2cd57-119">S_OK</span></span> 
  
> <span data-ttu-id="2cd57-120">As informações de erro foram retornadas.</span><span class="sxs-lookup"><span data-stu-id="2cd57-120">The error information was returned.</span></span>
    
<span data-ttu-id="2cd57-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="2cd57-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="2cd57-122">O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="2cd57-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2cd57-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2cd57-123">Remarks</span></span>

<span data-ttu-id="2cd57-124">O método **IMAPIProp:: GetLastError** fornece informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="2cd57-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="2cd57-125">Os clientes podem fornecer a seus usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2cd57-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="2cd57-126">Todas as implementações do **GetLastError** fornecidas pelo MAPI são implementações ANSI, exceto a implementação do [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd57-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="2cd57-127">O \*\*\*\* método GetLastError incluído no **IAddrBook** oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="2cd57-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2cd57-128">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="2cd57-128">Notes to implementers</span></span>

<span data-ttu-id="2cd57-129">Os detalhes da implementação de um provedor de transporte remoto desse método e as mensagens que esse método retorna são até o provedor de transporte, porque as condições de erro específicas que levam a vários valores HRESULT serão diferentes para diferentes transporte provedores.</span><span class="sxs-lookup"><span data-stu-id="2cd57-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2cd57-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="2cd57-130">Notes to callers</span></span>

<span data-ttu-id="2cd57-131">Você pode usar a estrutura **MAPIERROR** apontada pelo parâmetro _lppMAPIError_ , se GetLastError fornecer um, somente se o valor de retorno for S_OK. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="2cd57-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="2cd57-132">Às \*\*\*\* vezes, GetLastError não pode determinar qual é o último erro ou não tem mais a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="2cd57-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="2cd57-133">Nessa situação, um ponteiro para nulo é retornado em _lppMAPIError_ em vez disso.</span><span class="sxs-lookup"><span data-stu-id="2cd57-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="2cd57-134">Para liberar a memória da estrutura **MAPIERROR** , chame a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2cd57-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="2cd57-135">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="2cd57-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2cd57-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="2cd57-136">See also</span></span>



[<span data-ttu-id="2cd57-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="2cd57-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="2cd57-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="2cd57-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="2cd57-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="2cd57-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="2cd57-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2cd57-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="2cd57-141">Erros estendidos de MAPI</span><span class="sxs-lookup"><span data-stu-id="2cd57-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

