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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348059"
---
# <a name="hrcomposeeid"></a><span data-ttu-id="216e1-103">HrComposeEID</span><span class="sxs-lookup"><span data-stu-id="216e1-103">HrComposeEID</span></span>

  
  
<span data-ttu-id="216e1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="216e1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="216e1-105">Cria um identificador de entrada composto para um objeto, geralmente uma mensagem em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="216e1-105">Creates a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="216e1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="216e1-106">Header file:</span></span>  <br/> |<span data-ttu-id="216e1-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="216e1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="216e1-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="216e1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="216e1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="216e1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="216e1-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="216e1-110">Called by:</span></span>  <br/> |<span data-ttu-id="216e1-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="216e1-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="216e1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="216e1-112">Parameters</span></span>

 <span data-ttu-id="216e1-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="216e1-113">_psession_</span></span>
  
> <span data-ttu-id="216e1-114">no Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="216e1-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="216e1-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="216e1-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="216e1-116">no Tamanho, em bytes, da chave de registro do repositório de mensagens que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="216e1-116">[in] Size, in bytes, of the record key of the message store holding the message or other object.</span></span> <span data-ttu-id="216e1-117">Se zero for passado no parâmetro _cbStoreRecordKey_ , o parâmetro _ppEID_ apontará para uma cópia do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="216e1-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _ppEID_ parameter points to a copy of the object's entry identifier.</span></span> 
    
 <span data-ttu-id="216e1-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="216e1-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="216e1-119">no Ponteiro para a chave de registro do repositório de mensagens que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="216e1-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="216e1-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="216e1-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="216e1-121">no Tamanho, em bytes, do identificador de entrada da mensagem ou de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="216e1-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="216e1-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="216e1-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="216e1-123">no Ponteiro para o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="216e1-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="216e1-124">_pcbEID_</span><span class="sxs-lookup"><span data-stu-id="216e1-124">_pcbEID_</span></span>
  
> <span data-ttu-id="216e1-125">bota Ponteiro para o tamanho, em bytes, do identificador retornado.</span><span class="sxs-lookup"><span data-stu-id="216e1-125">[out] Pointer to the size, in bytes, of the returned identifier.</span></span> 
    
 <span data-ttu-id="216e1-126">_ppEID_</span><span class="sxs-lookup"><span data-stu-id="216e1-126">_ppEID_</span></span>
  
> <span data-ttu-id="216e1-127">bota Ponteiro para um ponteiro para o identificador de entrada retornado.</span><span class="sxs-lookup"><span data-stu-id="216e1-127">[out] Pointer to a pointer to the returned entry identifier.</span></span> <span data-ttu-id="216e1-128">Se o valor do parâmetro _cbStoreRecordKey_ for maior que zero, o parâmetro _ppEID_ apontará para um ponteiro para o identificador de entrada composta que é criado.</span><span class="sxs-lookup"><span data-stu-id="216e1-128">If the value of the  _cbStoreRecordKey_ parameter is greater than zero, the  _ppEID_ parameter points to a pointer to the compound entry identifier that is created.</span></span> <span data-ttu-id="216e1-129">Se _cbStoreRecordKey_ for zero, _ppEID_ apontará para um ponteiro para uma cópia do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="216e1-129">If  _cbStoreRecordKey_ is zero,  _ppEID_ points to a pointer to a copy of the object's entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="216e1-130">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="216e1-130">Return value</span></span>

<span data-ttu-id="216e1-131">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="216e1-131">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="216e1-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="216e1-132">Remarks</span></span>

<span data-ttu-id="216e1-133">Se a mensagem ou outro objeto para o qual o identificador de entrada composta estiver sendo criado residir em um repositório de mensagens, o identificador será criado a partir do identificador de entrada do objeto e da chave de registro da loja.</span><span class="sxs-lookup"><span data-stu-id="216e1-133">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="216e1-134">Se o objeto não estiver em um repositório, ou seja, se a contagem de bytes para a chave de registro de repositório passada no _cbStoreRecordKey_ for zero, o identificador de entrada do objeto será simplesmente copiado.</span><span class="sxs-lookup"><span data-stu-id="216e1-134">If the object is not in a store, that is, if the byte count for the store record key passed in  _cbStoreRecordKey_ is zero, the object's entry identifier is simply copied.</span></span> 
  
<span data-ttu-id="216e1-135">A função **HrComposeEID** permite que os aplicativos trabalhem com objetos em vários repositórios por meio do uso de identificadores de entrada compostos.</span><span class="sxs-lookup"><span data-stu-id="216e1-135">The **HrComposeEID** function enables applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="216e1-136">Um aplicativo pode chamar a função [HrDecomposeEID](hrdecomposeeid.md) para dividir o identificador de entrada composta em seus constituintes originais.</span><span class="sxs-lookup"><span data-stu-id="216e1-136">An application can call the [HrDecomposeEID](hrdecomposeeid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="216e1-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="216e1-137">See also</span></span>



[<span data-ttu-id="216e1-138">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="216e1-138">HrComposeMsgID</span></span>](hrcomposemsgid.md)
  
[<span data-ttu-id="216e1-139">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="216e1-139">HrDecomposeMsgID</span></span>](hrdecomposemsgid.md)

