---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Logs para o site de rede social usando a autenticação baseada em formulários.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770864"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="a28a5-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="a28a5-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="a28a5-104">Logs para o site de rede social usando a autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="a28a5-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="a28a5-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a28a5-105">Parameters</span></span>

<span data-ttu-id="a28a5-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="a28a5-106">_connectIn_</span></span>
  
> <span data-ttu-id="a28a5-107">[in] Uma string que é **Nulo**, uma URL para um formulário de logon na web, ou uma cadeia de caracteres que contém as credenciais de logon, dependendo do contexto no processo de logon, quando esse método é chamado.</span><span class="sxs-lookup"><span data-stu-id="a28a5-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="a28a5-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="a28a5-108">_connectOut_</span></span>
  
> <span data-ttu-id="a28a5-109">[out] Uma cadeia de caracteres que contém as credenciais de logon.</span><span class="sxs-lookup"><span data-stu-id="a28a5-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a28a5-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="a28a5-110">Remarks</span></span>

<span data-ttu-id="a28a5-111">Outlook Social Connector (OSC) chama o método **LogonWeb** somente se o provedor indica que ele oferece suporte a autenticação baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="a28a5-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="a28a5-112">O provedor indica que ele requer autenticação baseada em formulários, definindo **useLogonWebAuth** como **true** no XML de **recursos**.</span><span class="sxs-lookup"><span data-stu-id="a28a5-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="a28a5-113">Se o provedor define **useLogonWebAuth** como **false**, o OSC usará a autenticação básica e chama o método [ISocialSession::Logon](isocialsession-logon.md) .</span><span class="sxs-lookup"><span data-stu-id="a28a5-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="a28a5-114">Fazer logon em um site de rede social usando a autenticação baseada em formulários envolve chamando os métodos **LogonWeb** e [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) em uma ordem específica:</span><span class="sxs-lookup"><span data-stu-id="a28a5-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="a28a5-115">O OSC chama **LogonWeb** na primeira vez, passando **Nulo** para o parâmetro _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="a28a5-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="a28a5-116">O provedor gera o erro OSC_E_AUTH_ERROR para o OSC.</span><span class="sxs-lookup"><span data-stu-id="a28a5-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="a28a5-117">Em seguida, o OSC chama **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="a28a5-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="a28a5-118">O provedor retorna a URL adequada para uma página de logon no método **GetLogonUrl** .</span><span class="sxs-lookup"><span data-stu-id="a28a5-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="a28a5-119">O OSC usa a URL retornada pela **GetLogonUrl** para exibir a página de logon baseada em formulários.</span><span class="sxs-lookup"><span data-stu-id="a28a5-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="a28a5-120">O OSC chama **LogonWeb** uma segunda vez, passando a URL para o formulário de logon no parâmetro _connectIn_ .</span><span class="sxs-lookup"><span data-stu-id="a28a5-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="a28a5-121">Se a autenticação tiver êxito, o provedor retorna as credenciais de logon no parâmetro _connectOut_ para o OSC.</span><span class="sxs-lookup"><span data-stu-id="a28a5-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="a28a5-122">Se a autenticação falhar, o provedor gera o erro OSC_E_AUTH_ERROR para o OSC.</span><span class="sxs-lookup"><span data-stu-id="a28a5-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="a28a5-123">Se o provedor do OSC suporta logon usando as credenciais armazenadas em cache, ele especifica **useLogonCached** como **true** em **recursos** XML.</span><span class="sxs-lookup"><span data-stu-id="a28a5-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="a28a5-124">O provedor deve colocar qualquer credenciais de logon na cadeia de caracteres _connectOut_ que deseja que o provedor do OSC para armazenar nas conexões.</span><span class="sxs-lookup"><span data-stu-id="a28a5-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="a28a5-125">O OSC não interpretar a cadeia de caracteres _connectOut_ .</span><span class="sxs-lookup"><span data-stu-id="a28a5-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="a28a5-126">Depois que o OSC verifica que **useLogonCached** for **true**, o OSC criptografa a cadeia de caracteres para segurança antes de armazená-lo no registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="a28a5-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="a28a5-127">O OSC passa essa cadeia de caracteres para o parâmetro _connectIn_ em fazer logon rede social chamando [ISocialSession2::LogonCached](isocialsession2-logoncached.md)as tentativas posteriores.</span><span class="sxs-lookup"><span data-stu-id="a28a5-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="a28a5-128">Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a28a5-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a28a5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="a28a5-129">See also</span></span>

- [<span data-ttu-id="a28a5-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a28a5-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="a28a5-131">Autenticação baseada em formulários</span><span class="sxs-lookup"><span data-stu-id="a28a5-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

