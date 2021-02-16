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
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326191"
---
# <a name="openimsgsession"></a><span data-ttu-id="5daa0-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="5daa0-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="5daa0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5daa0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5daa0-105">Cria e abre uma sessão de mensagem que grupos as mensagens criadas dentro dela.</span><span class="sxs-lookup"><span data-stu-id="5daa0-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5daa0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5daa0-106">Header file:</span></span>  <br/> |<span data-ttu-id="5daa0-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="5daa0-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="5daa0-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5daa0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5daa0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5daa0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5daa0-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5daa0-110">Called by:</span></span>  <br/> |<span data-ttu-id="5daa0-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="5daa0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="5daa0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5daa0-112">Parameters</span></span>

 <span data-ttu-id="5daa0-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="5daa0-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="5daa0-114">[in] Ponteiro para um objeto alocador de memória expondo a interface [IMalloc OLE.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)</span><span class="sxs-lookup"><span data-stu-id="5daa0-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="5daa0-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span><span class="sxs-lookup"><span data-stu-id="5daa0-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="5daa0-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5daa0-116">_ulFlags_</span></span>
  
> <span data-ttu-id="5daa0-117">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5daa0-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="5daa0-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="5daa0-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="5daa0-119">[out] Ponteiro para um ponteiro para o objeto de sessão de mensagem retornado.</span><span class="sxs-lookup"><span data-stu-id="5daa0-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5daa0-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5daa0-120">Return value</span></span>

<span data-ttu-id="5daa0-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="5daa0-121">S_OK</span></span>
  
> <span data-ttu-id="5daa0-122">A sessão foi aberta.</span><span class="sxs-lookup"><span data-stu-id="5daa0-122">The session was opened.</span></span>
    
<span data-ttu-id="5daa0-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5daa0-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="5daa0-124">_lpMalloc_ ou  _lppMsgSess_ é NULL.</span><span class="sxs-lookup"><span data-stu-id="5daa0-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="5daa0-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="5daa0-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="5daa0-126">Sinalizadores inválidos foram passados.</span><span class="sxs-lookup"><span data-stu-id="5daa0-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="5daa0-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5daa0-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="5daa0-128">Ao chamar essa função, um cliente ou provedor de serviços define o sinalizador MAPI_UNICODE para criar arquivos .msg Unicode.</span><span class="sxs-lookup"><span data-stu-id="5daa0-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="5daa0-129">O arquivo [Imessage resultante](imessageimapiprop.md) mostra STORE_UNICODE_OK em sua PR_STORE_SUPPORT_MASK e dá suporte a propriedades Unicode.</span><span class="sxs-lookup"><span data-stu-id="5daa0-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5daa0-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="5daa0-130">Remarks</span></span>

<span data-ttu-id="5daa0-131">Uma sessão de mensagem é usada por aplicativos cliente e provedores de serviços que querem lidar com vários IMessage MAPI relacionados: objetos [IMAPIProp](imessageimapiprop.md) construídos com base em objetos **OLE IStorage** subjacentes.</span><span class="sxs-lookup"><span data-stu-id="5daa0-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="5daa0-132">O cliente ou provedor usa as funções **OpenIMsgSession** e [CloseIMsgSession](closeimsgsession.md) para quebrar a criação dessas mensagens dentro de uma sessão de mensagem.</span><span class="sxs-lookup"><span data-stu-id="5daa0-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="5daa0-133">Depois que a sessão de mensagem é aberta, o cliente ou provedor passa um ponteiro para ela em uma chamada para [OpenIMsgOnIStg](openimsgonistg.md) para criar um novo objeto **IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="5daa0-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="5daa0-134">Uma sessão de mensagem mantém o controle de todos os objetos **IMessage** **-on-IStorage** criados durante a sessão, além de todos os anexos e outras propriedades das mensagens.</span><span class="sxs-lookup"><span data-stu-id="5daa0-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="5daa0-135">Quando um cliente ou provedor chama **CloseIMsgSession**, ele fecha todos esses objetos.</span><span class="sxs-lookup"><span data-stu-id="5daa0-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="5daa0-136">Chamar **CloseIMsgSession** é a única maneira de fechar objetos **IMessage**-on-IStorage. </span><span class="sxs-lookup"><span data-stu-id="5daa0-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="5daa0-137">**OpenIMsgSession** é usado por clientes e provedores que exigem a capacidade de lidar com várias mensagens relacionadas como objetos OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="5daa0-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="5daa0-138">Se apenas uma dessas mensagens for aberta por vez, não será necessário controlar várias mensagens e nenhum motivo para criar uma sessão de mensagem com **OpenIMsgSession**.</span><span class="sxs-lookup"><span data-stu-id="5daa0-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="5daa0-139">Como ele está lidando com um objeto OLE subjacente, o MAPI precisa usar a alocação de memória OLE.</span><span class="sxs-lookup"><span data-stu-id="5daa0-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="5daa0-140">Para obter mais informações sobre objetos de armazenamento estruturado OLE e alocação de memória OLE, consulte [OLE e Transferência de Dados.](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)</span><span class="sxs-lookup"><span data-stu-id="5daa0-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

