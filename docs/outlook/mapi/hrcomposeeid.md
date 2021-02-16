---
title: HrComposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeEID
api_type:
- COM
ms.assetid: 8aba90d8-ea1f-4636-af80-17bfeadbdfa0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7de4fdefee67c79fb15ac28f821b015cdda6708d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429044"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="1dcc4-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="1dcc4-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="1dcc4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dcc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dcc4-105">Cria um identificador de entrada composto para um objeto, geralmente uma mensagem em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1dcc4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1dcc4-106">Header file:</span></span>  <br/> |<span data-ttu-id="1dcc4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1dcc4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1dcc4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1dcc4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1dcc4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1dcc4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1dcc4-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="1dcc4-110">Called by:</span></span>  <br/> |<span data-ttu-id="1dcc4-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="1dcc4-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeEID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  ULONG FAR * pcbEID,
  LPENTRYID FAR * ppEID
);
```

## <a name="parameters"></a><span data-ttu-id="1dcc4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1dcc4-112">Parameters</span></span>

 <span data-ttu-id="1dcc4-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-113">_psession_</span></span>
  
> <span data-ttu-id="1dcc4-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="1dcc4-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="1dcc4-116">[in] Tamanho, em bytes, da chave de registro do armazenamento de mensagens que mantém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="1dcc4-117">Se zero for passado no parâmetro  _cbStoreRecordKey,_ o parâmetro  _ppEID_ aponta para uma cópia do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="1dcc4-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="1dcc4-119">[in] Ponteiro para a tecla de registro do armazenamento de mensagens que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="1dcc4-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="1dcc4-121">[in] Tamanho, em bytes, do identificador de entrada da mensagem ou de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="1dcc4-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="1dcc4-123">[in] Ponteiro para o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="1dcc4-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-124">_pcbEID_</span></span>
  
> <span data-ttu-id="1dcc4-125">[out] Ponteiro para o tamanho, em bytes, do identificador retornado.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="1dcc4-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="1dcc4-126">_ppEID_</span></span>
  
> <span data-ttu-id="1dcc4-127">[out] Ponteiro para um ponteiro para o identificador de entrada retornado.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="1dcc4-128">Se o valor do parâmetro  _cbStoreRecordKey_ for maior que zero, o parâmetro  _ppEID_ aponta para um ponteiro para o identificador de entrada composto criado.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="1dcc4-129">Se  _cbStoreRecordKey_ for zero,  _ppEID_ aponta para um ponteiro para uma cópia do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1dcc4-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1dcc4-130">Return value</span></span>

<span data-ttu-id="1dcc4-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1dcc4-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="1dcc4-132">Remarks</span></span>

<span data-ttu-id="1dcc4-133">Se a mensagem ou outro objeto para o qual o identificador de entrada composta está sendo criado residir em um armazenamento de mensagens, o identificador será criado a partir do identificador de entrada do objeto e da chave de registro do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="1dcc4-134">Se o objeto não estiver em um repositório, ou seja, se a contagem de byte para a chave de registro do repositório passada em  _cbStoreRecordKey_ for zero, o identificador de entrada do objeto será simplesmente copiado.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="1dcc4-135">A **função HrComposeEID** permite que os aplicativos trabalhem com objetos em vários armazenamentos por meio do uso de identificadores de entrada compostos.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="1dcc4-136">Um aplicativo pode chamar [a função HrDecomposeEID](hrdecomposeeid.md) para dividir o identificador de entrada composta em seus componentes originais.</span><span class="sxs-lookup"><span data-stu-id="1dcc4-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1dcc4-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1dcc4-137">See also</span></span>



[<span data-ttu-id="1dcc4-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="1dcc4-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="1dcc4-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="1dcc4-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

