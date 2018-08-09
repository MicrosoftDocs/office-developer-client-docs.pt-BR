---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Logs para o site de rede social usando credenciais armazenadas em cache.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770871"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="41f6f-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="41f6f-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="41f6f-104">Logs para o site de rede social usando credenciais armazenadas em cache.</span><span class="sxs-lookup"><span data-stu-id="41f6f-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="41f6f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41f6f-105">Parameters</span></span>

<span data-ttu-id="41f6f-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="41f6f-106">_connectIn_</span></span>
  
> <span data-ttu-id="41f6f-107">[in] Uma cadeia de caracteres que pode ser vazia ou contém as credenciais de logon, dependendo do contexto no qual o OSC está chamando **LogonCached**.</span><span class="sxs-lookup"><span data-stu-id="41f6f-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="41f6f-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="41f6f-108">_userName_</span></span>
  
> <span data-ttu-id="41f6f-109">[in] Uma cadeia de caracteres que contém o nome de usuário.</span><span class="sxs-lookup"><span data-stu-id="41f6f-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="41f6f-110">_senha_</span><span class="sxs-lookup"><span data-stu-id="41f6f-110">_password_</span></span>
  
> <span data-ttu-id="41f6f-111">[in] Uma cadeia de caracteres que contém a senha do usuário.</span><span class="sxs-lookup"><span data-stu-id="41f6f-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="41f6f-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="41f6f-112">_connectOut_</span></span>
  
> <span data-ttu-id="41f6f-113">[out] Uma cadeia de caracteres opaca que contém as credenciais.</span><span class="sxs-lookup"><span data-stu-id="41f6f-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41f6f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="41f6f-114">Remarks</span></span>

<span data-ttu-id="41f6f-115">Este método é chamado para autenticação somente se **useLogonCached** estiver definida como **true** nas **capacidades** XML retornado pelo [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="41f6f-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="41f6f-116">Outlook Social Connector (OSC) chamará o **LogonCached**e passará uma sequência vazia para _connectIn_ e não vazias cadeias de caracteres de _nome de usuário_ e _senha_ .</span><span class="sxs-lookup"><span data-stu-id="41f6f-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="41f6f-117">O provedor usa o _nome de usuário_ e _senha_ para fazer logon na rede social e retorna um parâmetro opaco _connectOut_ para o OSC se a autenticação tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="41f6f-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="41f6f-118">Se a autenticação falhar, o provedor retorna o erro OSC_E_LOGON_FAILURE para o OSC.</span><span class="sxs-lookup"><span data-stu-id="41f6f-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="41f6f-119">O parâmetro _connectOut_ é uma sequência de caracteres opaca para o OSC e é passado para o parâmetro _connectIn_ as tentativas posteriores pelo OSC para fazer logon na rede social.</span><span class="sxs-lookup"><span data-stu-id="41f6f-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="41f6f-120">O provedor deve colocar qualquer credenciais na cadeia de caracteres _connectOut_ que deseja que o provedor do OSC para armazenar nas conexões.</span><span class="sxs-lookup"><span data-stu-id="41f6f-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="41f6f-121">O OSC não interpreta a cadeia de caracteres em _connectOut_e criptografa a cadeia de caracteres para fins de segurança antes de armazená-lo no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="41f6f-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="41f6f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="41f6f-122">See also</span></span>

- [<span data-ttu-id="41f6f-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41f6f-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

