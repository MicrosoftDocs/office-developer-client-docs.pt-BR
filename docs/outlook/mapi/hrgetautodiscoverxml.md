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
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347800"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="ac17a-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="ac17a-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="ac17a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac17a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac17a-105">Retorna um fluxo de Extensible Markup Language (XML) que representa informações recuperadas do serviço de descoberta automática de um servidor do Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="ac17a-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ac17a-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="ac17a-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac17a-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="ac17a-107">Exported by:</span></span>  <br/> |<span data-ttu-id="ac17a-108">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="ac17a-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="ac17a-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="ac17a-109">Called by:</span></span>  <br/> |<span data-ttu-id="ac17a-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="ac17a-110">Client</span></span>  <br/> |
|<span data-ttu-id="ac17a-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="ac17a-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ac17a-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="ac17a-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="ac17a-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ac17a-113">Parameters</span></span>

 <span data-ttu-id="ac17a-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="ac17a-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="ac17a-115">no Um endereço de email SMTP (Simple Mail Transfer Protocol) terminada em nulo da conta para a qual você deseja recuperar as informações de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="ac17a-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="ac17a-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="ac17a-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="ac17a-117">no Uma senha opcional para a conta especificada por _pwzAddress_.</span><span class="sxs-lookup"><span data-stu-id="ac17a-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="ac17a-118">Observe que a passagem de qualquer senha não terá efeito se a conta especificada por _pwzAddress_ não exigir uma senha.</span><span class="sxs-lookup"><span data-stu-id="ac17a-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="ac17a-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="ac17a-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="ac17a-120">no Um manipulador de eventos Win32 desdefinida que é opcional e pode ser usado para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="ac17a-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="ac17a-121">Para cancelar a operação, defina o evento e passe o manipulador de eventos como _hCancelEvent_; Passe **NULL** se você não quiser cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="ac17a-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="ac17a-122">Observe que passar um valor que não representa um manipulador de eventos não tem efeito e é ignorado pela função.</span><span class="sxs-lookup"><span data-stu-id="ac17a-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="ac17a-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac17a-123">_ulFlags_</span></span>
  
> <span data-ttu-id="ac17a-124">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="ac17a-124">[in] This parameter is not used.</span></span> <span data-ttu-id="ac17a-125">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="ac17a-125">It must be 0.</span></span>
    
 <span data-ttu-id="ac17a-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="ac17a-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="ac17a-127">bota Um ponteiro para um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) que contém o XML de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="ac17a-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="ac17a-128">Retorna **NULL** se a operação de descoberta automática falhar.</span><span class="sxs-lookup"><span data-stu-id="ac17a-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="ac17a-129">Você deve liberar o objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) quando tiver concluído.</span><span class="sxs-lookup"><span data-stu-id="ac17a-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="ac17a-130">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ac17a-130">Return values</span></span>

<span data-ttu-id="ac17a-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac17a-131">S_OK</span></span> 
  
- <span data-ttu-id="ac17a-132">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ac17a-132">The function call is successful.</span></span>
    
<span data-ttu-id="ac17a-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="ac17a-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="ac17a-134">_pwzAddress_ é **nulo** ou não é um endereço SMTP válido, ou _ppXmlStream_ é um ponteiro **nulo** para um objeto [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ac17a-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="ac17a-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ac17a-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="ac17a-136">O computador cliente não está conectado à rede, o computador cliente não está conectado a um servidor do Microsoft Exchange 2007, _pwzAddress_ não é uma conta em um servidor do Exchange 2007 ou _pwzAddress_ é uma conta que não dá suporte ao Exchange serviço de descoberta automática.</span><span class="sxs-lookup"><span data-stu-id="ac17a-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="ac17a-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="ac17a-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="ac17a-138">Um identificador de evento foi passado para _hCancelEvent_ para cancelar a operação.</span><span class="sxs-lookup"><span data-stu-id="ac17a-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="ac17a-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="ac17a-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="ac17a-140">O valor passado para _pwzAddress_ ou _pwzPassword_ é muito longo, de forma que ele estoura o buffer interno de tamanho de 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="ac17a-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

