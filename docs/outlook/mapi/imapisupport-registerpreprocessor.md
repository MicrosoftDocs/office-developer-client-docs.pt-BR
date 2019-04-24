---
title: IMAPISupportRegisterPreprocessor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.RegisterPreprocessor
api_type:
- COM
ms.assetid: 9b5659ab-2b49-41ab-92ce-ca343e35d670
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 58215de6cc4e9e68386f8f017839752acc6e1753
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326562"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="f82b1-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="f82b1-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="f82b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f82b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f82b1-105">Registra a função de pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="f82b1-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
```cpp
HRESULT RegisterPreprocessor(
LPMAPIUID lpMuid,
LPSTR lpszAdrType,
LPSTR lpszDLLName,
LPSTR lpszPreprocess,
LPSTR lpszRemovePreprocessInfo,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="f82b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f82b1-106">Parameters</span></span>

 <span data-ttu-id="f82b1-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="f82b1-107">_lpMuid_</span></span>
  
> <span data-ttu-id="f82b1-108">no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador que a função de pré-processador manipula.</span><span class="sxs-lookup"><span data-stu-id="f82b1-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="f82b1-109">O parâmetro _lpMuid_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f82b1-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f82b1-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="f82b1-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="f82b1-111">no Um ponteiro para o tipo de endereço das mensagens que a função Opera, como FAX, SMTP ou X500.</span><span class="sxs-lookup"><span data-stu-id="f82b1-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="f82b1-112">O parâmetro _lpszAdrType_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f82b1-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f82b1-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="f82b1-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="f82b1-114">no Um ponteiro para o nome da biblioteca de vínculo dinâmico (DLL) que contém o ponto de entrada para a função de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="f82b1-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="f82b1-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="f82b1-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="f82b1-116">no Um ponteiro para o nome da função de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="f82b1-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="f82b1-117">O parâmetro _lpszPreprocess_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f82b1-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f82b1-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="f82b1-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="f82b1-119">no Um ponteiro para o nome da função que remove as informações do pré-processador (uma função que está de acordo com o protótipo do [RemovePreprocessInfo](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="f82b1-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="f82b1-120">O parâmetro _lpszRemovePreprocessInfo_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="f82b1-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="f82b1-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f82b1-121">_ulFlags_</span></span>
  
> <span data-ttu-id="f82b1-122">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f82b1-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f82b1-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f82b1-123">Return value</span></span>

<span data-ttu-id="f82b1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f82b1-124">S_OK</span></span> 
  
> <span data-ttu-id="f82b1-125">A função de pré-processador foi registrada com êxito.</span><span class="sxs-lookup"><span data-stu-id="f82b1-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f82b1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="f82b1-126">Remarks</span></span>

<span data-ttu-id="f82b1-127">O método **IMAPISupport:: RegisterPreprocessor** é implementado apenas para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f82b1-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="f82b1-128">Os provedores de transporte chamam **RegisterPreprocessor** para registrar uma função de pré-processador (uma função que está em conformidade com o protótipo do [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="f82b1-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="f82b1-129">Uma função de pré-processador deve ser registrada antes que o spooler MAPI possa chamá-lo.</span><span class="sxs-lookup"><span data-stu-id="f82b1-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="f82b1-130">Os parâmetros _lpszPreprocess_, _lpszRemovePreprocessInfo_e _lpszDLLName_ devem apontar para cadeias de caracteres que podem ser usadas em conjunto com as chamadas para a função de **GetProcAddress** do Win32, permitindo a DLL do pré-processador ponto de entrada a ser chamado corretamente.</span><span class="sxs-lookup"><span data-stu-id="f82b1-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f82b1-131">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f82b1-131">Notes to callers</span></span>

<span data-ttu-id="f82b1-132">As chamadas para pré-processadors são específicas para a ordem do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="f82b1-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="f82b1-133">Isso significa que, se outro provedor de transporte antes do seu provedor puder lidar com uma mensagem, sua função de pré-processador não será chamada para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="f82b1-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="f82b1-134">Sua função de pré-processador será chamada somente para mensagens que você manipulará.</span><span class="sxs-lookup"><span data-stu-id="f82b1-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="f82b1-135">Você pode escrever funções de pré-processador para lidar com um identificador específico armazenado em uma estrutura [MAPIUID](mapiuid.md) ou um tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="f82b1-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="f82b1-136">Se você especificar uma estrutura **MAPIUID** no parâmetro _lpMuid_ e um tipo de endereço no parâmetro _lpszAdrType_ , sua função será chamada para destinatários de mensagens que correspondam ao **MAPIUID** ou ao tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="f82b1-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="f82b1-137">Se _lpMuid_ for nulo e _LPSZADRTYPE_ for não nulo, sua função será chamada somente para destinatários que tenham um endereço que corresponda ao tipo apontado por _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="f82b1-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="f82b1-138">Se _lpMuid_ for não nulo e _lpszAdrType_ for nulo, sua função será chamada para destinatários que correspondam a **MAPIUID**, independentemente do tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="f82b1-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="f82b1-139">Se ambos forem nulos, sua função será chamada para todos os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f82b1-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f82b1-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f82b1-140">See also</span></span>



[<span data-ttu-id="f82b1-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="f82b1-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="f82b1-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="f82b1-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="f82b1-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="f82b1-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="f82b1-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f82b1-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

