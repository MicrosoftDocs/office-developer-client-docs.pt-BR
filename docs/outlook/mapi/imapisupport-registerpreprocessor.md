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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 219c15fc00490983e970e4533f927cf4d91916b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767281"
---
# <a name="imapisupportregisterpreprocessor"></a><span data-ttu-id="5999f-103">IMAPISupport::RegisterPreprocessor</span><span class="sxs-lookup"><span data-stu-id="5999f-103">IMAPISupport::RegisterPreprocessor</span></span>

  
  
<span data-ttu-id="5999f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5999f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5999f-105">Registra função pré-processador de um provedor de transporte (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="5999f-105">Registers a transport provider's preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> 
  
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

## <a name="parameters"></a><span data-ttu-id="5999f-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5999f-106">Parameters</span></span>

 <span data-ttu-id="5999f-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="5999f-107">_lpMuid_</span></span>
  
> <span data-ttu-id="5999f-108">[in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador que manipula a função pré-processador.</span><span class="sxs-lookup"><span data-stu-id="5999f-108">[in] A pointer to the [MAPIUID](mapiuid.md) structure that contains the identifier that the preprocessor function handles.</span></span> <span data-ttu-id="5999f-109">O parâmetro _lpMuid_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5999f-109">The  _lpMuid_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5999f-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="5999f-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="5999f-111">[in] Um ponteiro para o tipo de endereço para as mensagens a função opera em, como X500, SMTP ou FAX.</span><span class="sxs-lookup"><span data-stu-id="5999f-111">[in] A pointer to the address type for the messages the function operates on, such as FAX, SMTP, or X500.</span></span> <span data-ttu-id="5999f-112">O parâmetro _lpszAdrType_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5999f-112">The  _lpszAdrType_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5999f-113">_lpszDLLName_</span><span class="sxs-lookup"><span data-stu-id="5999f-113">_lpszDLLName_</span></span>
  
> <span data-ttu-id="5999f-114">[in] Um ponteiro para o nome da biblioteca de vínculo dinâmico (DLL) que contém o ponto de entrada para a função de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="5999f-114">[in] A pointer to the name of the dynamic-link library (DLL) that contains the entry point for the preprocessor function.</span></span>
    
 <span data-ttu-id="5999f-115">_lpszPreprocess_</span><span class="sxs-lookup"><span data-stu-id="5999f-115">_lpszPreprocess_</span></span>
  
> <span data-ttu-id="5999f-116">[in] Um ponteiro para o nome da função pré-processador.</span><span class="sxs-lookup"><span data-stu-id="5999f-116">[in] A pointer to the name of the preprocessor function.</span></span> <span data-ttu-id="5999f-117">O parâmetro _lpszPreprocess_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5999f-117">The  _lpszPreprocess_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5999f-118">_lpszRemovePreprocessInfo_</span><span class="sxs-lookup"><span data-stu-id="5999f-118">_lpszRemovePreprocessInfo_</span></span>
  
> <span data-ttu-id="5999f-119">[in] Um ponteiro para o nome da função que removem informações pré-processador (uma função que está em conformidade com o protótipo [RemovePreprocessInfo](removepreprocessinfo.md) ).</span><span class="sxs-lookup"><span data-stu-id="5999f-119">[in] A pointer to the name of the function that removes preprocessor information (a function that conforms to the [RemovePreprocessInfo](removepreprocessinfo.md) prototype).</span></span> <span data-ttu-id="5999f-120">O parâmetro _lpszRemovePreprocessInfo_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="5999f-120">The  _lpszRemovePreprocessInfo_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="5999f-121">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5999f-121">_ulFlags_</span></span>
  
> <span data-ttu-id="5999f-122">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5999f-122">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5999f-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5999f-123">Return value</span></span>

<span data-ttu-id="5999f-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5999f-124">S_OK</span></span> 
  
> <span data-ttu-id="5999f-125">A função pré-processador foi registrada com êxito.</span><span class="sxs-lookup"><span data-stu-id="5999f-125">The preprocessor function was successfully registered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5999f-126">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="5999f-126">Remarks</span></span>

<span data-ttu-id="5999f-127">O método **IMAPISupport::RegisterPreprocessor** é implementado para transporte provedor suporte apenas os objetos.</span><span class="sxs-lookup"><span data-stu-id="5999f-127">The **IMAPISupport::RegisterPreprocessor** method is implemented for transport provider support objects only.</span></span> <span data-ttu-id="5999f-128">Provedores de transporte chamarem **RegisterPreprocessor** para registrar uma função pré-processador (uma função que está em conformidade com o protótipo [PreprocessMessage](preprocessmessage.md) ).</span><span class="sxs-lookup"><span data-stu-id="5999f-128">Transport providers call **RegisterPreprocessor** to register a preprocessor function (a function that conforms to the [PreprocessMessage](preprocessmessage.md) prototype).</span></span> <span data-ttu-id="5999f-129">Uma função pré-processador deve ser registrada antes do MAPI spooler pode chamá-lo.</span><span class="sxs-lookup"><span data-stu-id="5999f-129">A preprocessor function must be registered before the MAPI spooler can call it.</span></span> 
  
<span data-ttu-id="5999f-130">Os parâmetros _lpszPreprocess_, _lpszRemovePreprocessInfo_e _lpszDLLName_ devem apontar para as cadeias de caracteres que podem ser usadas em conjunto com as chamadas para a função Win32 **GetProcAddress** , permitindo que DLL do pré-processador ponto de entrada a ser chamado corretamente.</span><span class="sxs-lookup"><span data-stu-id="5999f-130">The  _lpszPreprocess_,  _lpszRemovePreprocessInfo_, and  _lpszDLLName_ parameters should all point to strings that can be used in conjunction with calls to the Win32 **GetProcAddress** function, allowing the preprocessor's DLL entry point to be called correctly.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5999f-131">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="5999f-131">Notes to callers</span></span>

<span data-ttu-id="5999f-132">Chamadas para pré-processador são específicas a ordem do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="5999f-132">Calls to preprocessors are specific to transport provider order.</span></span> <span data-ttu-id="5999f-133">Isso significa que se outro provedor de transporte, além do seu provedor for capaz de lidar com uma mensagem, sua função pré-processador não será chamada para essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="5999f-133">This means that if another transport provider ahead of your provider is able to handle a message, your preprocessor function will not be called for that message.</span></span> <span data-ttu-id="5999f-134">Somente para mensagens que você irá lidar com sua função pré-processador será chamada.</span><span class="sxs-lookup"><span data-stu-id="5999f-134">Your preprocessor function will be called only for messages that you will handle.</span></span>
  
<span data-ttu-id="5999f-135">Você pode escrever pré-processador funções para manipular um identificador específico armazenado em uma estrutura [MAPIUID](mapiuid.md) ou um tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="5999f-135">You can write preprocessor functions to handle either a specific identifier stored in a [MAPIUID](mapiuid.md) structure or a type of address.</span></span> <span data-ttu-id="5999f-136">Se você especificar ambas uma estrutura **MAPIUID** no parâmetro _lpMuid_ e um tipo de endereço no parâmetro _lpszAdrType_ , sua função será chamada para os destinatários da mensagem que correspondem a **MAPIUID** ou o tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="5999f-136">If you specify both a **MAPIUID** structure in the  _lpMuid_ parameter and an address type in the  _lpszAdrType_ parameter, your function will be called for message recipients that match either the **MAPIUID** or the address type.</span></span> <span data-ttu-id="5999f-137">Se _lpMuid_ é NULL e _lpszAdrType_ é não-nulo, sua função será chamada somente para os destinatários que tiverem um endereço que corresponde ao tipo apontado pela _lpszAdrType_.</span><span class="sxs-lookup"><span data-stu-id="5999f-137">If  _lpMuid_ is NULL and  _lpszAdrType_ is non-NULL, your function will be called only for recipients that have an address that matches the type pointed to by  _lpszAdrType_.</span></span> <span data-ttu-id="5999f-138">Se _lpMuid_ for não-nulos e _lpszAdrType_ é NULL, sua função será chamada para destinatários que correspondem a **MAPIUID**, independentemente de seu tipo de endereço.</span><span class="sxs-lookup"><span data-stu-id="5999f-138">If  _lpMuid_ is non-NULL and  _lpszAdrType_ is NULL, your function will be called for recipients that match **MAPIUID**, regardless of their address type.</span></span> <span data-ttu-id="5999f-139">Se ambos forem NULL, sua função é chamada para todos os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="5999f-139">If both are NULL, your function is called for all recipients of the message.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5999f-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="5999f-140">See also</span></span>



[<span data-ttu-id="5999f-141">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="5999f-141">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="5999f-142">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="5999f-142">PreprocessMessage</span></span>](preprocessmessage.md)
  
[<span data-ttu-id="5999f-143">RemovePreprocessInfo</span><span class="sxs-lookup"><span data-stu-id="5999f-143">RemovePreprocessInfo</span></span>](removepreprocessinfo.md)
  
[<span data-ttu-id="5999f-144">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5999f-144">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

