---
title: HrComposeMsgID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrComposeMsgID
api_type:
- COM
ms.assetid: bb76b147-6552-4cc4-920f-699170aea17f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3bcad4c236f71390f7a048eb66860720e9180e06
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582039"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="70b1c-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="70b1c-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="70b1c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70b1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70b1c-105">Cria uma cadeia de caracteres ASCII que representa um identificador de compostos de entrada para um objeto, geralmente em uma mensagem em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="70b1c-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70b1c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="70b1c-106">Header file:</span></span>  <br/> |<span data-ttu-id="70b1c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="70b1c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="70b1c-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="70b1c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="70b1c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="70b1c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="70b1c-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="70b1c-110">Called by:</span></span>  <br/> |<span data-ttu-id="70b1c-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="70b1c-111">Client applications</span></span>  <br/> |
   
```cpp
HrComposeMsgID(
  LPMAPISESSION psession,
  ULONG cbStoreRecordKey,
  LPBYTE pStoreRecordKey,
  ULONG cbMsgEID,
  LPENTRYID pMsgEID,
  LPSTR FAR * pszMsgID
);
```

## <a name="parameters"></a><span data-ttu-id="70b1c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70b1c-112">Parameters</span></span>

 <span data-ttu-id="70b1c-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="70b1c-113">_psession_</span></span>
  
> <span data-ttu-id="70b1c-114">[in] Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="70b1c-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="70b1c-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="70b1c-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="70b1c-116">[in] Tamanho, em bytes, da chave do registro do repositório de mensagem que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="70b1c-117">Se o parâmetro _cbStoreRecordKey_ é passado zero, os pontos de parâmetro _pszMsgID_ para uma cópia do identificador de entrada é convertido em texto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="70b1c-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="70b1c-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="70b1c-119">[in] Ponteiro para a chave de registro do repositório de mensagem que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="70b1c-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="70b1c-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="70b1c-121">[in] Tamanho, em bytes, do identificador de entrada de mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="70b1c-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="70b1c-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="70b1c-123">[in] Ponteiro para o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="70b1c-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="70b1c-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="70b1c-125">[out] Ponteiro para a cadeia de caracteres ASCII retornado.</span><span class="sxs-lookup"><span data-stu-id="70b1c-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="70b1c-126">Se o parâmetro _cbStoreRecordKey_ for maior do que zero, os pontos de parâmetro _pszMsgID_ a um identificador de entrada compostos convertidos em texto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="70b1c-127">Se _cbStoreRecordKey_ for zero, _pszMsgID_ pontos a um identificador de entrada noncompound é convertido em texto.</span><span class="sxs-lookup"><span data-stu-id="70b1c-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="70b1c-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="70b1c-128">Return value</span></span>

<span data-ttu-id="70b1c-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="70b1c-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70b1c-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="70b1c-130">Remarks</span></span>

<span data-ttu-id="70b1c-131">Se a mensagem ou outro objeto para o qual está sendo criado o identificador de entrada compostos residir em um armazenamento de mensagens, a sequência identifier é criada do identificador de entrada do objeto e a chave do registro da loja.</span><span class="sxs-lookup"><span data-stu-id="70b1c-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="70b1c-132">Se o objeto não estiver em um repositório, ou seja, se o número de bytes para a chave de registro do repositório passado no parâmetro _cbStoreRecordKey_ for zero, o identificador de entrada do objeto é simplesmente copiado e convertido em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="70b1c-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="70b1c-133">Chamar a função **HrComposeMsgID** é equivalente a chamar a função [HrComposeEID](hrcomposeeid.md) e, em seguida, a função [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="70b1c-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="70b1c-134">**HrComposeMsgID** permite que os aplicativos de cliente trabalhar com objetos em repositórios de vários devido ao uso de identificadores de entrada compostos.</span><span class="sxs-lookup"><span data-stu-id="70b1c-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="70b1c-135">Um aplicativo pode chamar a função [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir o identificador de entrada compostos em seus constituintes originais.</span><span class="sxs-lookup"><span data-stu-id="70b1c-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

