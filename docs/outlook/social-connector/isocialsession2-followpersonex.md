---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Adiciona a pessoa identificada pelos parâmetros emailAddresses e displayName como um amigo para o usuário conectado na rede social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339652"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="7d165-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="7d165-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="7d165-104">Adiciona a pessoa identificada pelos __ parâmetros EmailAddresses e _DisplayName_ como um amigo para o usuário conectado na rede social.</span><span class="sxs-lookup"><span data-stu-id="7d165-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="7d165-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d165-105">Parameters</span></span>

<span data-ttu-id="7d165-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="7d165-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="7d165-107">no Uma matriz que contém um ou vários endereços SMTP válidos para uma pessoa na rede social.</span><span class="sxs-lookup"><span data-stu-id="7d165-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="7d165-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="7d165-108">_displayName_</span></span>
  
> <span data-ttu-id="7d165-109">no Uma cadeia de caracteres que contém o nome de exibição da pessoa a ser adicionada como amigo.</span><span class="sxs-lookup"><span data-stu-id="7d165-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7d165-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d165-110">Remarks</span></span>

<span data-ttu-id="7d165-111">Se o Outlook Social Connector (OSC) fornecer mais do que no endereço SMTP na matriz no parâmetro **EmailAddresses** , o provedor do OSC poderá assumir que o primeiro elemento é o endereço SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="7d165-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="7d165-112">Se o provedor tiver definido o elemento **followPerson** como **true** no XML de **recursos** e nenhum dos elementos de EmailAddresses __ corresponder a um usuário na rede, o provedor deverá retornar o erro OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="7d165-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="7d165-113">Se o provedor tiver definido **followPerson** como **falso** em **recursos**, o provedor deverá retornar o erro OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="7d165-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="7d165-114">Se o método **FollowPersonEx** for bem-sucedido, o provedor poderá usar a cadeia de caracteres no parâmetro _DisplayName_ para endereçar a pessoa em qualquer email de confirmação de amigo subsequente, em vez de endereçar a pessoa pelo endereço SMTP.</span><span class="sxs-lookup"><span data-stu-id="7d165-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="7d165-115">Por outro lado, o provedor deve ser capaz de lidar com o OSC passando uma cadeia de caracteres vazia para o parâmetro _DisplayName_ .</span><span class="sxs-lookup"><span data-stu-id="7d165-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="7d165-116">Se o provedor implementar a interface [ISocialSession2](isocialsession2iunknown.md) e tiver definido **followPerson** como **true** no XML de recursos, o OSC chamará **FollowPersonEx** em vez de [ISocialSession:: followPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="7d165-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="7d165-117">Se o provedor tiver definido **followPerson** como **true** , mas não implementar a interface **ISocialSession2** ou **FOLLOWPERSONEX** retornar o erro OSC_E_NOTIMPL, o OSC chamará **ISocialSession:: followPerson**.</span><span class="sxs-lookup"><span data-stu-id="7d165-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d165-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d165-118">See also</span></span>

- [<span data-ttu-id="7d165-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d165-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

