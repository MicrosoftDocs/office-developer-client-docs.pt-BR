---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Faz o login no site da rede social usando a autenticação baseada em formulários.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430333"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="b6d35-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="b6d35-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="b6d35-104">Faz o login no site da rede social usando a autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="b6d35-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="b6d35-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6d35-105">Parameters</span></span>

<span data-ttu-id="b6d35-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="b6d35-106">_connectIn_</span></span>
  
> <span data-ttu-id="b6d35-107">[in] Uma cadeia de caracteres nula **,** uma URL para um formulário de logon na Web ou uma cadeia de caracteres que contém credenciais de logon, dependendo do contexto no processo de logon quando esse método é chamado.</span><span class="sxs-lookup"><span data-stu-id="b6d35-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="b6d35-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="b6d35-108">_connectOut_</span></span>
  
> <span data-ttu-id="b6d35-109">[out] Uma cadeia de caracteres que contém credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="b6d35-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6d35-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6d35-110">Remarks</span></span>

<span data-ttu-id="b6d35-111">O Outlook Social Connector (OSC) chama o **método LogonWeb** somente se o provedor indicar que ele oferece suporte à autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="b6d35-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="b6d35-112">O provedor indica que requer autenticação baseada em formulários definindo **useLogonWebAuth** como **verdadeiro** no XML para **recursos.**</span><span class="sxs-lookup"><span data-stu-id="b6d35-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="b6d35-113">Se o provedor definir **useLogonWebAuth** como **false**, o OSC usa autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md).</span><span class="sxs-lookup"><span data-stu-id="b6d35-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="b6d35-114">Fazer logon em um site de rede social usando autenticação baseada em formulários envolve chamar os métodos **LogonWeb** e [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) em uma ordem específica:</span><span class="sxs-lookup"><span data-stu-id="b6d35-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="b6d35-115">O OSC chama **LogonWeb** pela primeira vez, passando **nulo** para _o parâmetro connectIn._</span><span class="sxs-lookup"><span data-stu-id="b6d35-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="b6d35-116">O provedor gera o OSC_E_AUTH_ERROR erro para o OSC.</span><span class="sxs-lookup"><span data-stu-id="b6d35-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="b6d35-117">Em seguida, o OSC **chama GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="b6d35-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="b6d35-118">O provedor retorna a URL apropriada para uma página de logon no **método GetLogonUrl.**</span><span class="sxs-lookup"><span data-stu-id="b6d35-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="b6d35-119">O OSC usa a URL retornada **por GetLogonUrl** para exibir a página de logon baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="b6d35-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="b6d35-120">Em seguida, o OSC **chama LogonWeb** uma segunda vez, passando a URL para o formulário de logon no _parâmetro connectIn._</span><span class="sxs-lookup"><span data-stu-id="b6d35-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="b6d35-121">Se a autenticação for bem-sucedida, o provedor retornará credenciais de logon no  _parâmetro connectOut_ para o OSC.</span><span class="sxs-lookup"><span data-stu-id="b6d35-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="b6d35-122">Se a autenticação falhar, o provedor a OSC_E_AUTH_ERROR para o OSC.</span><span class="sxs-lookup"><span data-stu-id="b6d35-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="b6d35-123">Se o provedor OSC suportar o logon usando credenciais armazenadas em cache, ele **especificará useLogonCached** como **true** no XML **de recursos.**</span><span class="sxs-lookup"><span data-stu-id="b6d35-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="b6d35-124">O provedor deve colocar quaisquer credenciais de logon na cadeia de caracteres  _connectOut_ que o provedor deseja que o OSC armazene entre conexões.</span><span class="sxs-lookup"><span data-stu-id="b6d35-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="b6d35-125">O OSC não interpreta a _cadeia de caracteres connectOut._</span><span class="sxs-lookup"><span data-stu-id="b6d35-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="b6d35-126">Depois que o OSC verifica se **o uso deLogonCached** é **verdadeiro,** o OSC criptografa a cadeia de caracteres para segurança antes de armazenar no Registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="b6d35-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="b6d35-127">O OSC passa essa cadeia de caracteres para o parâmetro  _connectIn_ em tentativas subsequentes de fazer logon na rede social chamando [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="b6d35-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="b6d35-128">Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b6d35-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b6d35-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="b6d35-129">See also</span></span>

- [<span data-ttu-id="b6d35-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6d35-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="b6d35-131">Autenticação baseada em formulários</span><span class="sxs-lookup"><span data-stu-id="b6d35-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

