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
ms.openlocfilehash: f67dbb4d883f2f66099f2e2b9bc06b6c35b98236
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575830"
---
# <a name="imapipropgetlasterror"></a><span data-ttu-id="9a4e3-103">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="9a4e3-103">IMAPIProp::GetLastError</span></span>

  
  
<span data-ttu-id="9a4e3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a4e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a4e3-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="9a4e3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a4e3-106">Parameters</span></span>

 <span data-ttu-id="9a4e3-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="9a4e3-107">_hResult_</span></span>
  
> <span data-ttu-id="9a4e3-108">[in] Um identificador para o código de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-108">[in] A handle to the error code generated in the previous method call.</span></span>
    
 <span data-ttu-id="9a4e3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9a4e3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9a4e3-110">[in] Uma bitmask dos sinalizadores que indica o formato para o texto retornado na estrutura **MAPIERROR** apontada pela _lppMAPIError_.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-110">[in] A bitmask of flags that indicates the format for the text returned in the **MAPIERROR** structure pointed to by  _lppMAPIError_.</span></span> <span data-ttu-id="9a4e3-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="9a4e3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9a4e3-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9a4e3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9a4e3-113">As cadeias de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-113">The strings should be in Unicode format.</span></span> <span data-ttu-id="9a4e3-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-114">If the MAPI_UNICODE flag is not set, the strings should be in ANSI format.</span></span>
    
 <span data-ttu-id="9a4e3-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="9a4e3-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="9a4e3-116">[out] Um ponteiro para um ponteiro para a estrutura **MAPIERROR** que contém informações de versão, componente e contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-116">[out] A pointer to a pointer to the **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="9a4e3-117">O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma informação de erro para retornar.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-117">The  _lppMAPIError_ parameter can be set to NULL if there is no error information to return.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9a4e3-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9a4e3-118">Return value</span></span>

<span data-ttu-id="9a4e3-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a4e3-119">S_OK</span></span> 
  
> <span data-ttu-id="9a4e3-120">As informações de erro foi retornadas.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-120">The error information was returned.</span></span>
    
<span data-ttu-id="9a4e3-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9a4e3-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9a4e3-122">Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-122">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a4e3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a4e3-123">Remarks</span></span>

<span data-ttu-id="9a4e3-124">O método **IMAPIProp::GetLastError** fornece informações sobre uma chamada de método anterior que falharam.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-124">The **IMAPIProp::GetLastError** method supplies information about a prior method call that failed.</span></span> <span data-ttu-id="9a4e3-125">Clientes podem fornecer aos usuários informações detalhadas sobre o erro, incluindo os dados da estrutura de **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-125">Clients can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
<span data-ttu-id="9a4e3-126">Todas as implementações de **GetLastError** fornecido pelo MAPI são implementações ANSI, exceto para a implementação de [IAddrBook](iaddrbookimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4e3-126">All of the implementations of **GetLastError** provided by MAPI are ANSI implementations, except for the [IAddrBook](iaddrbookimapiprop.md) implementation.</span></span> <span data-ttu-id="9a4e3-127">O método **GetLastError** incluído **IAddrBook** oferece suporte a Unicode.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-127">The **GetLastError** method included with **IAddrBook** supports Unicode.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9a4e3-128">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="9a4e3-128">Notes to implementers</span></span>

<span data-ttu-id="9a4e3-129">Os detalhes de um controle remoto de transporte do provedor de implementação deste método e Cite mensagens que esse método retorna o provedor de transporte, porque as condições de erro específicas que levam a vários valores de HRESULT será diferentes para transporte diferentes provedores.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-129">The details of a remote transport provider's implementation of this method and what messages this method returns are up to the transport provider, because the particular error conditions that lead to various HRESULT values will be different for different transport providers.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9a4e3-130">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9a4e3-130">Notes to callers</span></span>

<span data-ttu-id="9a4e3-131">Você pode usar a estrutura **MAPIERROR** apontada pelo parâmetro _lppMAPIError_ , se **GetLastError** fornece um, apenas se o valor de retorno é S_OK.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-131">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter, if **GetLastError** supplies one, only if the return value is S_OK.</span></span> <span data-ttu-id="9a4e3-132">Às vezes **GetLastError** não pode determinar o que o último erro foi ou não tem nada mais a ser relatado sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-132">Sometimes **GetLastError** cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="9a4e3-133">Nessa situação, um ponteiro como NULL é retornado em _lppMAPIError_ , em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9a4e3-133">In this situation, a pointer to NULL is returned in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="9a4e3-134">Para liberar a memória para a estrutura **MAPIERROR** , chame a função de [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9a4e3-134">To release the memory for the **MAPIERROR** structure, call the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="9a4e3-135">Para obter mais informações sobre o método **GetLastError** , consulte [MAPI estendido erros](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="9a4e3-135">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9a4e3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a4e3-136">See also</span></span>



[<span data-ttu-id="9a4e3-137">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="9a4e3-137">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="9a4e3-138">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="9a4e3-138">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="9a4e3-139">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="9a4e3-139">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="9a4e3-140">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a4e3-140">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md)


[<span data-ttu-id="9a4e3-141">MAPI estendido erros</span><span class="sxs-lookup"><span data-stu-id="9a4e3-141">MAPI Extended Errors</span></span>](mapi-extended-errors.md)

