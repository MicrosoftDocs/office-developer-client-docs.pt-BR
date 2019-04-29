---
title: HrDecomposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrDecomposeMsgID
api_type:
- COM
ms.assetid: 5e6a9f3e-79be-4ffd-9d42-3a14cabb1435
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bff73ee5cf02680a2376106e21e0c743b995d336
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404432"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="336f5-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="336f5-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="336f5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="336f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="336f5-105">Separa a representação ASCII do identificador de entrada composta de um objeto, geralmente uma mensagem em um repositório de mensagens, no identificador de entrada desse objeto no repositório e no identificador de entrada da loja.</span><span class="sxs-lookup"><span data-stu-id="336f5-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="336f5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="336f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="336f5-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="336f5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="336f5-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="336f5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="336f5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="336f5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="336f5-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="336f5-110">Called by:</span></span>  <br/> |<span data-ttu-id="336f5-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="336f5-111">Client applications</span></span>  <br/> |
   
```cpp
HrDecomposeMsgID(
  LPMAPISESSION psession,
  LPSTR szMsgID,
  ULONG FAR * pcbStoreEID,
  LPENTRYID FAR * ppStoreEID,
  ULONG FAR * pcbMsgEID,
  LPENTRYID FAR * ppMsgEID
);
```

## <a name="parameters"></a><span data-ttu-id="336f5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="336f5-112">Parameters</span></span>

 <span data-ttu-id="336f5-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="336f5-113">_psession_</span></span>
  
> <span data-ttu-id="336f5-114">no Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="336f5-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="336f5-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="336f5-115">_szMsgID_</span></span>
  
> <span data-ttu-id="336f5-116">no A cadeia de caracteres que representa o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="336f5-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="336f5-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="336f5-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="336f5-118">bota Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagens que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="336f5-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="336f5-119">Se o parâmetro _szMsgID_ apontar para uma cadeia de caracteres de identificador de entrada não composta, o parâmetro _pcbStoreEID_ apontará para zero.</span><span class="sxs-lookup"><span data-stu-id="336f5-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="336f5-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="336f5-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="336f5-121">bota Ponteiro para um ponteiro para o identificador de entrada retornado do repositório de mensagens que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="336f5-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="336f5-122">Se o parâmetro _szMsgID_ apontar para um identificador de entrada não composta, NULL será retornado no parâmetro _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="336f5-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="336f5-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="336f5-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="336f5-124">bota Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto dentro de seu repositório.</span><span class="sxs-lookup"><span data-stu-id="336f5-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="336f5-125">Se o parâmetro _szMsgID_ apontar para uma cadeia de caracteres de identificador de entrada não composta, o parâmetro _pcbMsgEID_ será igual ao valor do parâmetro _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="336f5-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="336f5-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="336f5-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="336f5-127">bota Ponteiro para um ponteiro para a cadeia de caracteres de identificador de entrada retornada do objeto dentro de seu repositório.</span><span class="sxs-lookup"><span data-stu-id="336f5-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="336f5-128">Se o parâmetro _szMsgID_ apontar para um identificador de entrada não composta, _ppMsgEID_ apontará para um ponteiro para uma cópia convertida do identificador de entrada não composta.</span><span class="sxs-lookup"><span data-stu-id="336f5-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="336f5-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="336f5-129">Return value</span></span>

<span data-ttu-id="336f5-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="336f5-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="336f5-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="336f5-131">Remarks</span></span>

<span data-ttu-id="336f5-132">Se o identificador especificado pelo parâmetro _szMsgID_ for composto, ele será convertido de ASCII e dividido no identificador de entrada do objeto no repositório de mensagens e no identificador de entrada da loja.</span><span class="sxs-lookup"><span data-stu-id="336f5-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="336f5-133">Cadeias de caracteres de identificador de entrada não compostos são apenas convertidos e copiados.</span><span class="sxs-lookup"><span data-stu-id="336f5-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="336f5-134">A cadeia de caracteres de identificador composto a ser separada é normalmente uma criada pela função [HrComposeMsgID](hrcomposemsgid.md) .</span><span class="sxs-lookup"><span data-stu-id="336f5-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="336f5-135">Chamar a função **HrDecomposeMsgID** é equivalente a chamar a função [HrEntryIDFromSz](hrentryidfromsz.md) e, em seguida, a função [HrDecomposeEID](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="336f5-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

