---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Adiciona a pessoa identificada pelo parâmetro emailAddress como um amigo para o usuário conectado na rede social.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285361"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="6aa29-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="6aa29-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="6aa29-104">Adiciona a pessoa identificada pelo parâmetro _EmailAddress_ como um amigo para o usuário conectado na rede social.</span><span class="sxs-lookup"><span data-stu-id="6aa29-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="6aa29-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6aa29-105">Parameters</span></span>

<span data-ttu-id="6aa29-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="6aa29-106">_emailAddress_</span></span>
  
> <span data-ttu-id="6aa29-107">no Uma cadeia de caracteres que contém um endereço de email de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="6aa29-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6aa29-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="6aa29-108">Remarks</span></span>

<span data-ttu-id="6aa29-109">O parâmetro _EmailAddress_ deve ser um endereço SMTP válido.</span><span class="sxs-lookup"><span data-stu-id="6aa29-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="6aa29-110">Se o provedor do Outlook Social Connector (OSC) tiver definido o método **followPerson** como **true** nos **recursos**e o argumento para _EmailAddress_ não corresponder a um usuário na rede, o provedor deverá retornar o OSC_E_NOT_FOUND erros.</span><span class="sxs-lookup"><span data-stu-id="6aa29-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="6aa29-111">Se o provedor tiver definido **followPerson** como **falso** em **recursos**, o provedor deverá retornar o erro OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="6aa29-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="6aa29-112">Se o provedor implementar a interface [ISocialSession2](isocialsession2iunknown.md) e tiver definido **followPerson** como **true** nos **recursos**, o OSC chamará [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) em vez de \*\*ISocialSession:: followPerson \*\*.</span><span class="sxs-lookup"><span data-stu-id="6aa29-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="6aa29-113">Se o provedor não implementar a interface **ISocialSession2** ou **ISocialSession2:: FollowPersonEx** retorna o erro OSC_E_NOTIMPL, o OSC chamará **ISocialSession:: FollowPerson** , desde que o provedor tenha definido \*\* followPerson\*\* como **verdadeiro** em **recursos**.</span><span class="sxs-lookup"><span data-stu-id="6aa29-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="6aa29-114">Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6aa29-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="6aa29-115">Ao decidir se deve implementar **ISocalSession:: FollowPerson** ou **ISocialSession2:: FollowPersonEx**, você deve considerar se o provedor precisa de outros métodos no **ISocialSession2**e se você pode usar o _ parâmetro djsplayName_ em **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="6aa29-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6aa29-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="6aa29-116">See also</span></span>

- [<span data-ttu-id="6aa29-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6aa29-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

