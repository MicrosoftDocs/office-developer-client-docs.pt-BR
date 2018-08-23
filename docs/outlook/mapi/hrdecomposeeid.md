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
ms.openlocfilehash: 7cae156e29503c8b50755c99023805aa6d14e704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573366"
---
# <a name="hrdecomposeeid"></a><span data-ttu-id="74628-103">HrDecomposeEID</span><span class="sxs-lookup"><span data-stu-id="74628-103">HrDecomposeEID</span></span>

  
  
<span data-ttu-id="74628-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74628-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74628-105">Separa o identificador de entrada compostos de um objeto, geralmente em uma mensagem em um armazenamento de mensagens, no identificador de entrada desse objeto no repositório e o identificador de entrada da loja.</span><span class="sxs-lookup"><span data-stu-id="74628-105">Separates the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="74628-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="74628-106">Header file:</span></span>  <br/> |<span data-ttu-id="74628-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="74628-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="74628-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="74628-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="74628-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="74628-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="74628-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="74628-110">Called by:</span></span>  <br/> |<span data-ttu-id="74628-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="74628-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="74628-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74628-112">Parameters</span></span>

 <span data-ttu-id="74628-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="74628-113">_psession_</span></span>
  
> <span data-ttu-id="74628-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="74628-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="74628-115">_cbEID_</span><span class="sxs-lookup"><span data-stu-id="74628-115">_cbEID_</span></span>
  
> <span data-ttu-id="74628-116">[in] Tamanho, em bytes, do identificador de entrada compostos sejam separados.</span><span class="sxs-lookup"><span data-stu-id="74628-116">[in] Size, in bytes, of the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="74628-117">_pEID_</span><span class="sxs-lookup"><span data-stu-id="74628-117">_pEID_</span></span>
  
> <span data-ttu-id="74628-118">[in] Ponteiro para o identificador de entrada compostos sejam separados.</span><span class="sxs-lookup"><span data-stu-id="74628-118">[in] Pointer to the compound entry identifier to be separated.</span></span> 
    
 <span data-ttu-id="74628-119">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="74628-119">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="74628-120">[out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagem que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="74628-120">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="74628-121">Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, em seguida, o parâmetro _pcbStoreEID_ aponta para um valor de zero.</span><span class="sxs-lookup"><span data-stu-id="74628-121">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbStoreEID_ parameter points to a value of zero.</span></span> 
    
 <span data-ttu-id="74628-122">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="74628-122">_ppStoreEID_</span></span>
  
> <span data-ttu-id="74628-123">[out] Ponteiro para um ponteiro para o identificador retornado de entrada do repositório de mensagem que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="74628-123">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="74628-124">Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, NULL é retornado no parâmetro _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="74628-124">If the  _pEID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="74628-125">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="74628-125">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="74628-126">[out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="74628-126">[out] Pointer to the returned size, in bytes, of the entry identifier of the object.</span></span> <span data-ttu-id="74628-127">Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, o parâmetro _pcbMsgEID_ é igual ao valor do parâmetro _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="74628-127">If the  _pEID_ parameter points to a noncompound entry identifier, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="74628-128">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="74628-128">_ppMsgEID_</span></span>
  
> <span data-ttu-id="74628-129">[out] Ponteiro para um ponteiro para o identificador de entrada retornados do objeto.</span><span class="sxs-lookup"><span data-stu-id="74628-129">[out] Pointer to a pointer to the returned entry identifier of the object.</span></span> <span data-ttu-id="74628-130">Se o parâmetro _pEID_ aponta para um identificador de entrada noncompound, _ppMsgEID_ aponta para um ponteiro para uma cópia do identificador de entrada noncompound.</span><span class="sxs-lookup"><span data-stu-id="74628-130">If the  _pEID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="74628-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="74628-131">Return value</span></span>

<span data-ttu-id="74628-132">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="74628-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74628-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="74628-133">Remarks</span></span>

<span data-ttu-id="74628-134">Se o identificador especificado pelo parâmetro _pEID_ for composto, ele é dividido no identificador de entrada do objeto dentro de seu armazenamento de mensagens e o identificador de entrada da loja.</span><span class="sxs-lookup"><span data-stu-id="74628-134">If the identifier specified by the  _pEID_ parameter is compound, it is split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="74628-135">Cadeias de caracteres de identificador de entrada noncompound simplesmente são copiadas.</span><span class="sxs-lookup"><span data-stu-id="74628-135">Noncompound entry identifier strings are simply copied.</span></span> <span data-ttu-id="74628-136">O identificador composto sejam separados é geralmente uma criada pela função [HrComposeEID](hrcomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="74628-136">The compound identifier to be separated is usually one created by the [HrComposeEID](hrcomposeeid.md) function.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="74628-137">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="74628-137">Notes to callers</span></span>

<span data-ttu-id="74628-138">A memória que contém o parâmetro _pEID_ é liberada após a conclusão bem-sucedida dessa função.</span><span class="sxs-lookup"><span data-stu-id="74628-138">The memory that holds the  _pEID_ parameter is released upon successful completion of this function.</span></span> <span data-ttu-id="74628-139">A implementação de chamada é responsável por liberar memória para os parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="74628-139">The calling implementation is responsible for freeing memory for the output parameters.</span></span> 
  

