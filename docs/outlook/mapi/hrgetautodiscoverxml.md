---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: da466fc9add8cbc385014782f31749d3b6522da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766781"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="7caf1-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="7caf1-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="7caf1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7caf1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7caf1-105">Retorna um fluxo de Extensible Markup Language (XML) que representa as informações recuperadas do serviço de descoberta automática de um servidor Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="7caf1-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7caf1-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="7caf1-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7caf1-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="7caf1-107">Exported by:</span></span>  <br/> |<span data-ttu-id="7caf1-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="7caf1-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="7caf1-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="7caf1-109">Called by:</span></span>  <br/> |<span data-ttu-id="7caf1-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="7caf1-110">Client</span></span>  <br/> |
|<span data-ttu-id="7caf1-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="7caf1-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="7caf1-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="7caf1-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="7caf1-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7caf1-113">Parameters</span></span>

 <span data-ttu-id="7caf1-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="7caf1-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="7caf1-115">[in] Um terminada em nulo Simple Mail Transfer Protocol (SMTP) endereço de email da conta para o qual você deseja recuperar as informações de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="7caf1-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="7caf1-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="7caf1-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="7caf1-117">[in] Uma senha opcional para a conta especificada pelo _pwzAddress_.</span><span class="sxs-lookup"><span data-stu-id="7caf1-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="7caf1-118">Observe que passar qualquer senha não tem efeito se a conta especificada pelo _pwzAddress_ não exigir uma senha.</span><span class="sxs-lookup"><span data-stu-id="7caf1-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="7caf1-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="7caf1-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="7caf1-120">[in] Um não definido identificador de eventos de Win32 que é opcional e pode ser usado para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="7caf1-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="7caf1-121">Para cancelar a operação, defina o evento e passar o identificador de eventos como _hCancelEvent_; passe **null** se não desejar cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="7caf1-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="7caf1-122">Observação passando um valor que não representam um identificador de eventos não tem efeito e é ignorada pela função.</span><span class="sxs-lookup"><span data-stu-id="7caf1-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="7caf1-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7caf1-123">_ulFlags_</span></span>
  
> <span data-ttu-id="7caf1-124">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="7caf1-124">[in] This parameter is not used.</span></span> <span data-ttu-id="7caf1-125">Ela deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="7caf1-125">It must be 0.</span></span>
    
 <span data-ttu-id="7caf1-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="7caf1-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="7caf1-127">[out] Um ponteiro para um objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) que contém a XML de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="7caf1-127">[out] A pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="7caf1-128">Retorna **null** se a operação de descoberta automática falhar.</span><span class="sxs-lookup"><span data-stu-id="7caf1-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="7caf1-129">Você deve liberar o objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) quando terminar com ele.</span><span class="sxs-lookup"><span data-stu-id="7caf1-129">You must release the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7caf1-130">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="7caf1-130">Return values</span></span>

<span data-ttu-id="7caf1-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="7caf1-131">S_OK</span></span> 
  
- <span data-ttu-id="7caf1-132">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7caf1-132">The function call is successful.</span></span>
    
<span data-ttu-id="7caf1-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7caf1-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="7caf1-134">_pwzAddress_ é **Nulo** ou não é um endereço SMTP válido, ou _ppXmlStream_ é um ponteiro **Nulo** para um objeto [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7caf1-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="7caf1-135">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7caf1-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="7caf1-136">Computador cliente não está conectado à rede, computador cliente não está conectado a um servidor Microsoft Exchange 2007, _pwzAddress_ não for uma conta em um servidor Exchange 2007 ou _pwzAddress_ é uma conta que não oferece suporte para Exchange serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="7caf1-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="7caf1-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="7caf1-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="7caf1-138">Um identificador de eventos foi passado para _hCancelEvent_ para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="7caf1-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="7caf1-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="7caf1-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="7caf1-140">O valor passado para _pwzAddress_ ou _pwzPassword_ é muito longo, de forma que ele estouros de buffer interno do tamanho de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="7caf1-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

