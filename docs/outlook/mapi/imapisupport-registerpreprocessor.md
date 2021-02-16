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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404894"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="ee720-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="ee720-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="ee720-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee720-105">Registra a função de pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage).](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="ee720-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="ee720-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee720-106">Parameters</span></span>

 <span data-ttu-id="ee720-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="ee720-107">_lpMuid_</span></span>
  
> <span data-ttu-id="ee720-108">[in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador que a função de pré-processador trata.</span><span class="sxs-lookup"><span data-stu-id="ee720-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="ee720-109">O  _parâmetro lpMuid_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ee720-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ee720-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="ee720-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="ee720-111">[in] Um ponteiro para o tipo de endereço das mensagens em que a função opera, como FAX, SMTP ou X500.</span><span class="sxs-lookup"><span data-stu-id="ee720-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="ee720-112">O  _parâmetro lpszAdrType_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ee720-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ee720-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="ee720-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="ee720-114">[in] Um ponteiro para o nome da biblioteca de vínculo dinâmico (DLL) que contém o ponto de entrada para a função de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="ee720-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="ee720-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="ee720-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="ee720-116">[in] Um ponteiro para o nome da função de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="ee720-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="ee720-117">O  _parâmetro lpszPreprocess_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ee720-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ee720-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="ee720-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="ee720-119">[in] Um ponteiro para o nome da função que remove as informações do pré-processador (uma função que está em conformidade com o protótipo [RemovePreprocessInfo).](removepreprocessinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ee720-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="ee720-120">O  _parâmetro lpszRemovePreprocessInfo_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="ee720-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="ee720-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ee720-121">_ulFlags_</span></span>
  
> <span data-ttu-id="ee720-122">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ee720-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ee720-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ee720-123">Return value</span></span>

<span data-ttu-id="ee720-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee720-124">S_OK</span></span> 
  
> <span data-ttu-id="ee720-125">A função de pré-processador foi registrada com êxito.</span><span class="sxs-lookup"><span data-stu-id="ee720-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee720-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee720-126">Remarks</span></span>

<span data-ttu-id="ee720-127">O **método IMAPISupport::RegisterPreprocessor** é implementado somente para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ee720-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="ee720-128">Os provedores de transporte **chamam RegisterPreprocessor** para registrar uma função de pré-processador (uma função que está em conformidade com o protótipo [PreprocessMessage).](preprocessmessage.md)</span><span class="sxs-lookup"><span data-stu-id="ee720-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="ee720-129">Uma função de pré-processador deve ser registrada antes que o spooler MAPI possa chamá-la.</span><span class="sxs-lookup"><span data-stu-id="ee720-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="ee720-130">Os  _parâmetros lpszPreprocess_,  _lpszRemovePreprocessInfo_ e  _lpszDLLName_ devem apontar para cadeias de caracteres que podem ser usadas em conjunto com chamadas para a função Win32 **GetProcAddress,** permitindo que o ponto de entrada DLL do pré-processador seja chamado corretamente.</span><span class="sxs-lookup"><span data-stu-id="ee720-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee720-131">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ee720-131">Notes to callers</span></span>

<span data-ttu-id="ee720-132">Chamadas para pré-processadores são específicas para a ordem do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="ee720-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="ee720-133">Isso significa que, se outro provedor de transporte à frente do provedor for capaz de manipular uma mensagem, sua função de pré-processador não será chamada para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="ee720-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="ee720-134">Sua função de pré-processador será chamada somente para mensagens que você manipulará.</span><span class="sxs-lookup"><span data-stu-id="ee720-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="ee720-135">Você pode escrever funções de pré-processador para manipular um identificador específico armazenado em uma estrutura [MAPIUID](mapiuid.md) ou um tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="ee720-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="ee720-136">Se você especificar uma estrutura **MAPIUID** no parâmetro  _lpMuid_ e um tipo de endereço no parâmetro  _lpszAdrType,_ sua função será chamada para destinatários de mensagem que corresponderem ao **MAPIUID** ou ao tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="ee720-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="ee720-137">Se  _lpMuid_ for NULL e  _lpszAdrType_ for diferente de NULL, sua função será chamada somente para destinatários que tenham um endereço que corresponde ao tipo apontado por  _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="ee720-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="ee720-138">Se  _lpMuid_ for non-NULL e  _lpszAdrType_ for NULL, sua função será chamada para destinatários que corresponderem a **MAPIUID**, independentemente do tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="ee720-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="ee720-139">Se ambos são NULL, sua função é chamada para todos os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="ee720-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ee720-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee720-140">See also</span></span>



[<span data-ttu-id="ee720-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="ee720-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="ee720-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="ee720-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="ee720-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="ee720-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="ee720-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee720-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

