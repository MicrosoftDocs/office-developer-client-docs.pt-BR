---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e7f652e7426792d8b4c878b7f6738439aec65348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768173"
---
# <a name="openimsgsession"></a><span data-ttu-id="f9b34-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="f9b34-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="f9b34-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9b34-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9b34-105">Cria e abre uma sessão de mensagem que agrupa as mensagens criadas com ela.</span><span class="sxs-lookup"><span data-stu-id="f9b34-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9b34-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f9b34-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9b34-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="f9b34-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="f9b34-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f9b34-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9b34-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f9b34-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f9b34-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f9b34-110">Called by:</span></span>  <br/> |<span data-ttu-id="f9b34-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f9b34-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="f9b34-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f9b34-112">Parameters</span></span>

 <span data-ttu-id="f9b34-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="f9b34-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="f9b34-114">[in] Ponteiro para um objeto de alocador de memória expondo a interface OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9b34-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="f9b34-115">MAPI deve usar esse método de alocação ao trabalhar com a interface OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f9b34-115">MAPI needs to use this allocation method when working with the OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) interface.</span></span> 
    
 <span data-ttu-id="f9b34-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9b34-116">_ulFlags_</span></span>
  
> <span data-ttu-id="f9b34-117">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f9b34-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="f9b34-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="f9b34-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="f9b34-119">[out] Ponteiro para um ponteiro para o objeto de sessão de mensagem retornada.</span><span class="sxs-lookup"><span data-stu-id="f9b34-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9b34-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f9b34-120">Return value</span></span>

<span data-ttu-id="f9b34-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9b34-121">S_OK</span></span>
  
> <span data-ttu-id="f9b34-122">A sessão foi aberta.</span><span class="sxs-lookup"><span data-stu-id="f9b34-122">The session was opened.</span></span>
    
<span data-ttu-id="f9b34-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f9b34-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="f9b34-124">_lpMalloc_ ou _lppMsgSess_ é nulo.</span><span class="sxs-lookup"><span data-stu-id="f9b34-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="f9b34-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="f9b34-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="f9b34-126">Sinalizadores inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="f9b34-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="f9b34-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9b34-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="f9b34-128">Ao chamar essa função, um cliente ou serviço provedor define o sinalizador MAPI_UNICODE para criar os arquivos do. msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="f9b34-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="f9b34-129">O arquivo resultante de [Imessage](imessageimapiprop.md) mostra STORE_UNICODE_OK no seu PR_STORE_SUPPORT_MASK e oferece suporte a Unicode propriedades.</span><span class="sxs-lookup"><span data-stu-id="f9b34-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f9b34-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9b34-130">Remarks</span></span>

<span data-ttu-id="f9b34-131">Uma sessão de mensagens é usada pelos aplicativos cliente e provedores de serviço que deseja lidar com vários relacionados MAPI [IMessage: IMAPIProp](imessageimapiprop.md) objetos construídos sobre objetos OLE **IStorage** subjacentes.</span><span class="sxs-lookup"><span data-stu-id="f9b34-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="f9b34-132">O cliente ou o provedor usa as funções **OpenIMsgSession** e [CloseIMsgSession](closeimsgsession.md) para quebrar a criação dessas mensagens de uma sessão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f9b34-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="f9b34-133">Depois que a sessão de mensagens é aberta, o cliente ou o provedor passa um ponteiro para ele em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo **IMessage**- on - objeto **|** .</span><span class="sxs-lookup"><span data-stu-id="f9b34-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="f9b34-134">Uma sessão de mensagens rastreia de todos os **IMessage**- on - objetos **IStorage** criados durante a duração da sessão, além de todos os anexos e outras propriedades das mensagens.</span><span class="sxs-lookup"><span data-stu-id="f9b34-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="f9b34-135">Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos.</span><span class="sxs-lookup"><span data-stu-id="f9b34-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="f9b34-136">Chamar o **CloseIMsgSession** é a única maneira de fechar **IMessage**- on - **IStorage** objetos.</span><span class="sxs-lookup"><span data-stu-id="f9b34-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="f9b34-137">**OpenIMsgSession** é usado por clientes e provedores que requerem a capacidade de lidar com várias mensagens relacionadas como objetos OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="f9b34-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="f9b34-138">Se houver apenas uma dessas mensagens para ser aberto por vez, não há nenhuma necessidade para controlar várias mensagens e não há motivo para criar uma sessão de mensagem com **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="f9b34-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="f9b34-139">Porque ele está lidando com um objeto OLE subjacente, MAPI deve usar a alocação de memória do OLE.</span><span class="sxs-lookup"><span data-stu-id="f9b34-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="f9b34-140">Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória do OLE, consulte [OLE e transferência de dados](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="f9b34-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

