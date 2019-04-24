---
title: IABLogonGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.GetLastError
api_type:
- COM
ms.assetid: d157e29e-7731-4e47-b4a7-e8622b223001
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 311299b00143667b3f2fb22bd7be6c3a52c7141d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349025"
---
# <a name="iablogongetlasterror"></a><span data-ttu-id="379dd-103">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="379dd-103">IABLogon::GetLastError</span></span>

  
  
<span data-ttu-id="379dd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="379dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="379dd-105">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="379dd-105">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous address book provider error.</span></span> 
  
```cpp
HRESULT GetLastError(
  HRESULT hResult,
  ULONG ulFlags,
  LPMAPIERROR FAR * lppMAPIError
);
```

## <a name="parameters"></a><span data-ttu-id="379dd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="379dd-106">Parameters</span></span>

 <span data-ttu-id="379dd-107">_And_</span><span class="sxs-lookup"><span data-stu-id="379dd-107">_hResult_</span></span>
  
> <span data-ttu-id="379dd-108">no Um identificador para o valor de erro gerado na chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="379dd-108">[in] A handle to the error value generated in the previous method call.</span></span>
    
 <span data-ttu-id="379dd-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="379dd-109">_ulFlags_</span></span>
  
> <span data-ttu-id="379dd-110">no Uma bitmask de sinalizadores que controla o tipo de cadeia de caracteres retornada.</span><span class="sxs-lookup"><span data-stu-id="379dd-110">[in] A bitmask of flags that controls the type of strings returned.</span></span> <span data-ttu-id="379dd-111">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="379dd-111">The following flag can be set:</span></span>
    
<span data-ttu-id="379dd-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="379dd-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="379dd-113">As cadeias de caracteres na estrutura **MAPIERROR** retornada no parâmetro _lppMAPIError_ estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="379dd-113">The strings in the **MAPIERROR** structure returned in the  _lppMAPIError_ parameter are in Unicode format.</span></span> <span data-ttu-id="379dd-114">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="379dd-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="379dd-115">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="379dd-115">_lppMAPIError_</span></span>
  
> <span data-ttu-id="379dd-116">bota Um ponteiro para um ponteiro para uma estrutura **MAPIERROR** que contém a versão, o componente e informações de contexto para o erro.</span><span class="sxs-lookup"><span data-stu-id="379dd-116">[out] A pointer to a pointer to a **MAPIERROR** structure that contains version, component, and context information for the error.</span></span> <span data-ttu-id="379dd-117">O parâmetro _lppMAPIError_ pode ser definido como nulo se o provedor não puder fornecer uma estrutura **MAPIERROR** com as informações apropriadas.</span><span class="sxs-lookup"><span data-stu-id="379dd-117">The  _lppMAPIError_ parameter can be set to NULL if the provider cannot supply a **MAPIERROR** structure with appropriate information.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="379dd-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="379dd-118">Return value</span></span>

<span data-ttu-id="379dd-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="379dd-119">S_OK</span></span> 
  
> <span data-ttu-id="379dd-120">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="379dd-120">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="379dd-121">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="379dd-121">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="379dd-122">O sinalizador MAPI_UNICODE foi definido e o provedor de catálogo de endereços não é compatível com Unicode, ou o MAPI_UNICODE não foi definido e o provedor de catálogo de endereços oferece suporte somente a Unicode.</span><span class="sxs-lookup"><span data-stu-id="379dd-122">Either the MAPI_UNICODE flag was set and the address book provider does not support Unicode, or MAPI_UNICODE was not set and the address book provider supports only Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="379dd-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="379dd-123">Remarks</span></span>

<span data-ttu-id="379dd-124">Os provedores de catálogos \*\*\*\* de endereços implementam o método GetLastError para fornecer informações sobre uma chamada de método anterior que falhou.</span><span class="sxs-lookup"><span data-stu-id="379dd-124">Address book providers implement the **GetLastError** method to supply information about a prior method call that failed.</span></span> <span data-ttu-id="379dd-125">Os chamadores podem fornecer aos usuários informações detalhadas sobre o erro incluindo os dados da estrutura **MAPIERROR** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="379dd-125">Callers can provide their users with detailed information about the error by including the data from the **MAPIERROR** structure in a dialog box.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="379dd-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="379dd-126">Notes to callers</span></span>

<span data-ttu-id="379dd-127">Você pode usar a estrutura **MAPIERROR** indicada pelo parâmetro _lppMAPIError_ se o provedor de catálogo de endereços fornecer a estrutura e somente se **GetLastError** retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="379dd-127">You can use the **MAPIERROR** structure pointed to by the  _lppMAPIError_ parameter if the address book provider supplies the structure and only if **GetLastError** returns S_OK.</span></span> <span data-ttu-id="379dd-128">Às vezes, o provedor do catálogo de endereços não pode determinar qual é o último erro ou não tem mais a relatar sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="379dd-128">Sometimes the address book provider cannot determine what the last error was or has nothing more to report about the error.</span></span> <span data-ttu-id="379dd-129">Nessa situação, o provedor do catálogo de endereços retorna um ponteiro para nulo no _lppMAPIError_ .</span><span class="sxs-lookup"><span data-stu-id="379dd-129">In this situation, the address book provider returns a pointer to NULL in  _lppMAPIError_ instead.</span></span> 
  
<span data-ttu-id="379dd-130">Para obter mais informações sobre \*\*\*\* o método GetLastError, consulte [MAPI Extended Errors](mapi-extended-errors.md).</span><span class="sxs-lookup"><span data-stu-id="379dd-130">For more information about the **GetLastError** method, see [MAPI Extended Errors](mapi-extended-errors.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="379dd-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="379dd-131">See also</span></span>



[<span data-ttu-id="379dd-132">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="379dd-132">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="379dd-133">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="379dd-133">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="379dd-134">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="379dd-134">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

