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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3095907498b1ce7ae6b3666e0678dd0c5f76c23e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766772"
---
# <a name="hrdecomposemsgid"></a><span data-ttu-id="5c2dd-103">HrDecomposeMsgID</span><span class="sxs-lookup"><span data-stu-id="5c2dd-103">HrDecomposeMsgID</span></span>

  
  
<span data-ttu-id="5c2dd-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c2dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c2dd-105">Separa a representação ASCII do identificador de entrada compostos de um objeto, geralmente em uma mensagem em um armazenamento de mensagens para o identificador de entrada desse objeto no repositório e o identificador de entrada da loja.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-105">Separates the ASCII representation of the compound entry identifier of an object, usually a message in a message store, into the entry identifier of that object in the store and the store's entry identifier.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c2dd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5c2dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="5c2dd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="5c2dd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5c2dd-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="5c2dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5c2dd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5c2dd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5c2dd-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="5c2dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="5c2dd-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="5c2dd-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="5c2dd-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="5c2dd-112">Parameters</span></span>

 <span data-ttu-id="5c2dd-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="5c2dd-113">_psession_</span></span>
  
> <span data-ttu-id="5c2dd-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="5c2dd-115">_szMsgID_</span><span class="sxs-lookup"><span data-stu-id="5c2dd-115">_szMsgID_</span></span>
  
> <span data-ttu-id="5c2dd-116">[in] A cadeia de caracteres representando o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-116">[in] The string representing the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="5c2dd-117">_pcbStoreEID_</span><span class="sxs-lookup"><span data-stu-id="5c2dd-117">_pcbStoreEID_</span></span>
  
> <span data-ttu-id="5c2dd-118">[out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do repositório de mensagem que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-118">[out] Pointer to the returned size, in bytes, of the entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="5c2dd-119">Se o parâmetro _szMsgID_ aponta para um identificador de entrada noncompound cadeia de caracteres, em seguida, os pontos de parâmetro _pcbStoreEID_ como zero.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-119">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbStoreEID_ parameter points to zero.</span></span> 
    
 <span data-ttu-id="5c2dd-120">_ppStoreEID_</span><span class="sxs-lookup"><span data-stu-id="5c2dd-120">_ppStoreEID_</span></span>
  
> <span data-ttu-id="5c2dd-121">[out] Ponteiro para um ponteiro para o identificador retornado de entrada do repositório de mensagem que contém o objeto.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-121">[out] Pointer to a pointer to the returned entry identifier of the message store that contains the object.</span></span> <span data-ttu-id="5c2dd-122">Se o parâmetro _szMsgID_ aponta para um identificador de entrada noncompound, NULL é retornado no parâmetro _ppStoreEID_ .</span><span class="sxs-lookup"><span data-stu-id="5c2dd-122">If the  _szMsgID_ parameter points to a noncompound entry identifier, NULL is returned in the  _ppStoreEID_ parameter.</span></span> 
    
 <span data-ttu-id="5c2dd-123">_pcbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5c2dd-123">_pcbMsgEID_</span></span>
  
> <span data-ttu-id="5c2dd-124">[out] Ponteiro para o tamanho retornado, em bytes, do identificador de entrada do objeto dentro de seu armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-124">[out] Pointer to the returned size, in bytes, of the entry identifier of the object within its store.</span></span> <span data-ttu-id="5c2dd-125">Se o parâmetro _szMsgID_ aponta para uma cadeia de caracteres do identificador de entrada noncompound, o parâmetro _pcbMsgEID_ é igual ao valor do parâmetro _cbEID_ .</span><span class="sxs-lookup"><span data-stu-id="5c2dd-125">If the  _szMsgID_ parameter points to a noncompound entry identifier string, then the  _pcbMsgEID_ parameter is equal to the value of the  _cbEID_ parameter.</span></span> 
    
 <span data-ttu-id="5c2dd-126">_ppMsgEID_</span><span class="sxs-lookup"><span data-stu-id="5c2dd-126">_ppMsgEID_</span></span>
  
> <span data-ttu-id="5c2dd-127">[out] Ponteiro para um ponteiro para a cadeia de caracteres de identificador retornado de entrada do objeto dentro de seu armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-127">[out] Pointer to a pointer to the returned entry identifier string of the object within its store.</span></span> <span data-ttu-id="5c2dd-128">Se o parâmetro _szMsgID_ aponta para um identificador de entrada noncompound, _ppMsgEID_ aponta para um ponteiro para uma cópia convertida do identificador de entrada noncompound.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-128">If the  _szMsgID_ parameter points to a noncompound entry identifier,  _ppMsgEID_ points to a pointer to a converted copy of the noncompound entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5c2dd-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5c2dd-129">Return value</span></span>

<span data-ttu-id="5c2dd-130">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-130">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c2dd-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c2dd-131">Remarks</span></span>

<span data-ttu-id="5c2dd-132">Se o identificador especificado pelo parâmetro _szMsgID_ for composto, ele é convertido de ASCII e dividido o identificador de entrada do objeto dentro de seu armazenamento de mensagens e o identificador de entrada da loja.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-132">If the identifier specified by the  _szMsgID_ parameter is compound, it is converted from ASCII and split into the entry identifier of the object within its message store and the store's entry identifier.</span></span> <span data-ttu-id="5c2dd-133">Cadeias de caracteres de identificador de entrada noncompound simplesmente são convertidas e copiadas.</span><span class="sxs-lookup"><span data-stu-id="5c2dd-133">Noncompound entry identifier strings are simply converted and copied.</span></span> <span data-ttu-id="5c2dd-134">A cadeia de caracteres de identificador compostos sejam separados é geralmente uma criada pela função [HrComposeMsgID](hrcomposemsgid.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2dd-134">The compound identifier string to be separated is usually one created by the [HrComposeMsgID](hrcomposemsgid.md) function.</span></span> 
  
<span data-ttu-id="5c2dd-135">Chamar a função **HrDecomposeMsgID** é equivalente a chamar a função [HrEntryIDFromSz](hrentryidfromsz.md) e, em seguida, a função [HrDecomposeEID](hrdecomposeeid.md) .</span><span class="sxs-lookup"><span data-stu-id="5c2dd-135">Calling the **HrDecomposeMsgID** function is equivalent to calling the [HrEntryIDFromSz](hrentryidfromsz.md) function and then the [HrDecomposeEID](hrdecomposeeid.md) function.</span></span> 
  

