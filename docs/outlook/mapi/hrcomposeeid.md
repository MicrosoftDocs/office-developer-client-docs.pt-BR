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
ms.openlocfilehash: a9aa6deeca930da82db61ba517796bfbc0676467
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766769"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="5d8d3-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="5d8d3-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="5d8d3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5d8d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5d8d3-105">Cria um identificador compostos de entrada para um objeto, geralmente em uma mensagem em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5d8d3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5d8d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="5d8d3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5d8d3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5d8d3-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="5d8d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5d8d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5d8d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5d8d3-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="5d8d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="5d8d3-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="5d8d3-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5d8d3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d8d3-112">Parameters</span></span>

 <span data-ttu-id="5d8d3-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-113">_psession_</span></span>
  
> <span data-ttu-id="5d8d3-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="5d8d3-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="5d8d3-116">[in] Tamanho, em bytes, da chave do registro do armazenamento de mensagens, mantendo a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="5d8d3-117">Se o parâmetro _cbStoreRecordKey_ é passado zero, o parâmetro _ppEID_ aponta para uma cópia do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="5d8d3-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="5d8d3-119">[in] Ponteiro para a chave de registro do repositório de mensagem que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="5d8d3-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="5d8d3-121">[in] Tamanho, em bytes, do identificador de entrada de mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="5d8d3-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="5d8d3-123">[in] Ponteiro para o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="5d8d3-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-124">_pcbEID_</span></span>
  
> <span data-ttu-id="5d8d3-125">[out] Ponteiro para o tamanho, em bytes, do identificador retornado.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="5d8d3-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="5d8d3-126">_ppEID_</span></span>
  
> <span data-ttu-id="5d8d3-127">[out] Ponteiro para um ponteiro para o identificador de entrada retornados.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="5d8d3-128">Se o valor do parâmetro _cbStoreRecordKey_ for maior do que zero, o parâmetro _ppEID_ aponta para um ponteiro para o identificador de entrada compostos que é criado.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="5d8d3-129">Se _cbStoreRecordKey_ for zero, _ppEID_ aponta para um ponteiro para uma cópia do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5d8d3-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5d8d3-130">Return value</span></span>

<span data-ttu-id="5d8d3-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5d8d3-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d8d3-132">Remarks</span></span>

<span data-ttu-id="5d8d3-133">Se a mensagem ou outro objeto para o qual está sendo criado o identificador de entrada compostos residir em um armazenamento de mensagens, o identificador é criado do identificador de entrada do objeto e a chave do registro da loja.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="5d8d3-134">Se o objeto não estiver em um repositório, ou seja, se o número de bytes para a chave de registro do repositório passada em _cbStoreRecordKey_ for zero, o identificador de entrada do objeto é simplesmente copiado.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="5d8d3-135">A função **HrComposeEID** permite que os aplicativos trabalhar com objetos em repositórios de vários devido ao uso de identificadores de entrada compostos.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="5d8d3-136">Um aplicativo pode chamar a função [HrDecomposeEID](hrdecomposeeid.md) para dividir o identificador de entrada compostos em seus constituintes originais.</span><span class="sxs-lookup"><span data-stu-id="5d8d3-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5d8d3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="5d8d3-137">See also</span></span>



[<span data-ttu-id="5d8d3-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="5d8d3-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="5d8d3-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="5d8d3-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

