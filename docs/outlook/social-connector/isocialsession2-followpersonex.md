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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429828"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="965fa-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="965fa-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="965fa-104">Adiciona a pessoa identificada pelos parâmetros  _emailAddresses_ e  _displayName_ como um amigo do usuário conectado na rede social.</span><span class="sxs-lookup"><span data-stu-id="965fa-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="965fa-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="965fa-105">Parameters</span></span>

<span data-ttu-id="965fa-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="965fa-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="965fa-107">[in] Uma matriz que contém um ou vários endereços SMTP válidos para uma pessoa na rede social.</span><span class="sxs-lookup"><span data-stu-id="965fa-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="965fa-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="965fa-108">_displayName_</span></span>
  
> <span data-ttu-id="965fa-109">[in] Uma cadeia de caracteres que contém o nome de exibição da pessoa a ser adicionada como um amigo.</span><span class="sxs-lookup"><span data-stu-id="965fa-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="965fa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="965fa-110">Remarks</span></span>

<span data-ttu-id="965fa-111">Se o Outlook Social Connector (OSC) fornece mais do que no endereço SMTP na matriz no parâmetro **emailAddresses,** o provedor OSC pode assumir que o primeiro elemento é o endereço SMTP principal.</span><span class="sxs-lookup"><span data-stu-id="965fa-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="965fa-112">Se o provedor tiver definido o elemento **followPerson** como **true** no **XML** de recursos e nenhum dos elementos de  _emailAddresses_ corresponder a um usuário na rede, o provedor deverá retornar o erro OSC_E_NOT_FOUND.</span><span class="sxs-lookup"><span data-stu-id="965fa-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="965fa-113">Se o provedor definiu **followPerson como** **falso** **nos** recursos, o provedor deve retornar o OSC_E_FAIL erro.</span><span class="sxs-lookup"><span data-stu-id="965fa-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="965fa-114">Se o método **FollowPersonEx** for bem-sucedido, o provedor poderá usar a cadeia de caracteres no parâmetro  _displayName_ para endereçar a pessoa em qualquer email subsequente de confirmação de amigo, em vez de endereçamento à pessoa pelo endereço SMTP.</span><span class="sxs-lookup"><span data-stu-id="965fa-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="965fa-115">Por outro lado, o provedor deve ser capaz de manipular o OSC passando uma cadeia de caracteres vazia para o _parâmetro displayName._</span><span class="sxs-lookup"><span data-stu-id="965fa-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="965fa-116">Se o provedor implementa a interface [ISocialSession2](isocialsession2iunknown.md) e definiu **followPerson** como **true** no XML de recursos, o OSC chama **FollowPersonEx** em vez de [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="965fa-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="965fa-117">Se o provedor definiu **followPerson** como **true,** mas não implementa a interface **ISocialSession2,** ou **FollowPersonEx** retorna o erro OSC_E_NOTIMPL, o OSC chama **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="965fa-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="965fa-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="965fa-118">See also</span></span>

- [<span data-ttu-id="965fa-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="965fa-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

