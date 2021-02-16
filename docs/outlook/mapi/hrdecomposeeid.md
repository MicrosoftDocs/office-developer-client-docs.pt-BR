---
title: HrDecomposeEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeEID
api_type:
- COM
ms.assetid: 4847838a-2ad8-4927-8f78-7fa5c8eb54eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d3ef8b61b6042d9c3e715168d9131a74facef000
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436108"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="e611c-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="e611c-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="e611c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e611c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e611c-105">Separa o identificador de entrada composta de um objeto, geralmente uma mensagem em um armazenamento de mensagens, no identificador de entrada desse objeto no armazenamento e no identificador de entrada do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e611c-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e611c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e611c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e611c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e611c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e611c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e611c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e611c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e611c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e611c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e611c-110">Called by:</span></span>  <br/> |<span data-ttu-id="e611c-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="e611c-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeEID(
  LPMAPISESSION psession,
  ULONG cbEID,
  LPENTRYID pEID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="e611c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e611c-112">Parameters</span></span>

 <span data-ttu-id="e611c-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="e611c-113">_psession_</span></span>
  
> <span data-ttu-id="e611c-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="e611c-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="e611c-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="e611c-115">_cbEID_</span></span>
  
> <span data-ttu-id="e611c-116">[in] Tamanho, em bytes, do identificador de entrada composto a ser separado.</span><span class="sxs-lookup"><span data-stu-id="e611c-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="e611c-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="e611c-117">_pEID_</span></span>
  
> <span data-ttu-id="e611c-118">[in] Ponteiro para o identificador de entrada composta a ser separado.</span><span class="sxs-lookup"><span data-stu-id="e611c-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="e611c-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="e611c-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="e611c-120">[out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do armazenamento de mensagens que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="e611c-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="e611c-121">Se o  _parâmetro pEID_ aponta para um identificador de entrada não encontrado, o parâmetro  _pcbStoreEID_ aponta para um valor zero.</span><span class="sxs-lookup"><span data-stu-id="e611c-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="e611c-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="e611c-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="e611c-123">[out] Ponteiro para um ponteiro para o identificador de entrada retornado do armazenamento de mensagens que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="e611c-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="e611c-124">Se o _parâmetro pEID_ aponta para um identificador de entrada não encontrado, NULL é retornado no _parâmetro ppStoreEID._</span><span class="sxs-lookup"><span data-stu-id="e611c-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="e611c-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="e611c-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="e611c-126">[out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="e611c-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="e611c-127">Se o parâmetro _pEID_ aponta para um identificador de entrada não encontrado, o parâmetro _pcbMsgEID_ é igual ao valor do parâmetro _cbEID._</span><span class="sxs-lookup"><span data-stu-id="e611c-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="e611c-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="e611c-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="e611c-129">[out] Ponteiro para um ponteiro para o identificador de entrada retornado do objeto.</span><span class="sxs-lookup"><span data-stu-id="e611c-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="e611c-130">Se o parâmetro  _pEID_ aponta para um identificador de entrada não encontrado,  _ppMsgEID_ aponta para um ponteiro para uma cópia do identificador de entrada não encontrado.</span><span class="sxs-lookup"><span data-stu-id="e611c-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e611c-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e611c-131">Return value</span></span>

<span data-ttu-id="e611c-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e611c-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e611c-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e611c-133">Remarks</span></span>

<span data-ttu-id="e611c-134">Se o identificador especificado pelo parâmetro  _pEID_ for composto, ele será dividido no identificador de entrada do objeto no armazenamento de mensagens e no identificador de entrada do armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e611c-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="e611c-135">As cadeias de caracteres do identificador de entrada não-computador são simplesmente copiadas.</span><span class="sxs-lookup"><span data-stu-id="e611c-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="e611c-136">O identificador composto a ser separado geralmente é aquele criado pela [função HrComposeEID.](hrcomposeeid.md)</span><span class="sxs-lookup"><span data-stu-id="e611c-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e611c-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e611c-137">Notes to callers</span></span>

<span data-ttu-id="e611c-138">A memória que contém o  _parâmetro pEID_ é liberada após a conclusão bem-sucedida dessa função.</span><span class="sxs-lookup"><span data-stu-id="e611c-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="e611c-139">A implementação da chamada é responsável por liberar memória para os parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="e611c-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

