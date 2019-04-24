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
ms.openlocfilehash: c035780d3d790d94551860a418401e63da1c2151
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348045"
---
# <a name="hrcomposemsgid"></a><span data-ttu-id="27848-103">HrComposeMsgID</span><span class="sxs-lookup"><span data-stu-id="27848-103">HrComposeMsgID</span></span>

  
  
<span data-ttu-id="27848-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27848-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27848-105">Cria uma cadeia de caracteres ASCII representando um identificador de entrada composto para um objeto, geralmente uma mensagem em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="27848-105">Creates an ASCII string representing a compound entry identifier for an object, usually a message in a message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="27848-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="27848-106">Header file:</span></span>  <br/> |<span data-ttu-id="27848-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="27848-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="27848-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="27848-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="27848-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="27848-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="27848-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="27848-110">Called by:</span></span>  <br/> |<span data-ttu-id="27848-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="27848-111">Client applications</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="27848-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27848-112">Parameters</span></span>

 <span data-ttu-id="27848-113">_psession_</span><span class="sxs-lookup"><span data-stu-id="27848-113">_psession_</span></span>
  
> <span data-ttu-id="27848-114">no Ponteiro para a sessão em uso pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="27848-114">[in] Pointer to the session in use by the client application.</span></span> 
    
 <span data-ttu-id="27848-115">_cbStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="27848-115">_cbStoreRecordKey_</span></span>
  
> <span data-ttu-id="27848-116">no Tamanho, em bytes, da chave de registro do repositório de mensagens que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="27848-116">[in] Size, in bytes, of the record key of the message store that contains the message or other object.</span></span> <span data-ttu-id="27848-117">Se zero for passado no parâmetro _cbStoreRecordKey_ , o parâmetro _pszMsgID_ apontará para uma cópia do identificador de entrada convertido em texto.</span><span class="sxs-lookup"><span data-stu-id="27848-117">If zero is passed in the  _cbStoreRecordKey_ parameter, the  _pszMsgID_ parameter points to a copy of the entry identifier converted to text.</span></span> 
    
 <span data-ttu-id="27848-118">_pStoreRecordKey_</span><span class="sxs-lookup"><span data-stu-id="27848-118">_pStoreRecordKey_</span></span>
  
> <span data-ttu-id="27848-119">no Ponteiro para a chave de registro do repositório de mensagens que contém a mensagem ou outro objeto.</span><span class="sxs-lookup"><span data-stu-id="27848-119">[in] Pointer to the record key of the message store that contains the message or other object.</span></span> 
    
 <span data-ttu-id="27848-120">_cbMsgEID_</span><span class="sxs-lookup"><span data-stu-id="27848-120">_cbMsgEID_</span></span>
  
> <span data-ttu-id="27848-121">no Tamanho, em bytes, do identificador de entrada da mensagem ou de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="27848-121">[in] Size, in bytes, of the entry identifier of the message or other object.</span></span> 
    
 <span data-ttu-id="27848-122">_pMsgEID_</span><span class="sxs-lookup"><span data-stu-id="27848-122">_pMsgEID_</span></span>
  
> <span data-ttu-id="27848-123">no Ponteiro para o identificador de entrada do objeto.</span><span class="sxs-lookup"><span data-stu-id="27848-123">[in] Pointer to the entry identifier of the object.</span></span> 
    
 <span data-ttu-id="27848-124">_pszMsgID_</span><span class="sxs-lookup"><span data-stu-id="27848-124">_pszMsgID_</span></span>
  
> <span data-ttu-id="27848-125">bota Ponteiro para a cadeia de caracteres ASCII retornada.</span><span class="sxs-lookup"><span data-stu-id="27848-125">[out] Pointer to the returned ASCII string.</span></span> <span data-ttu-id="27848-126">Se o parâmetro _cbStoreRecordKey_ for maior que zero, o parâmetro _pszMsgID_ apontará para um identificador de entrada composto convertido em texto.</span><span class="sxs-lookup"><span data-stu-id="27848-126">If the  _cbStoreRecordKey_ parameter is greater than zero, the  _pszMsgID_ parameter points to a compound entry identifier converted to text.</span></span> <span data-ttu-id="27848-127">Se _cbStoreRecordKey_ for zero, _pszMsgID_ apontará para um identificador de entrada não composto convertido em texto.</span><span class="sxs-lookup"><span data-stu-id="27848-127">If  _cbStoreRecordKey_ is zero,  _pszMsgID_ points to a noncompound entry identifier converted to text.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27848-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="27848-128">Return value</span></span>

<span data-ttu-id="27848-129">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="27848-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27848-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="27848-130">Remarks</span></span>

<span data-ttu-id="27848-131">Se a mensagem ou outro objeto para o qual o identificador de entrada composta estiver sendo criado residir em um repositório de mensagens, a cadeia de caracteres do identificador será criada a partir do identificador de entrada do objeto e da chave de registro da loja.</span><span class="sxs-lookup"><span data-stu-id="27848-131">If the message or other object for which the compound entry identifier is being created resides in a message store, the identifier string is created from the object's entry identifier and the store's record key.</span></span> <span data-ttu-id="27848-132">Se o objeto não estiver em um repositório, ou seja, se a contagem de bytes para a chave do registro de repositório passada no parâmetro _cbStoreRecordKey_ for zero, o identificador de entrada do objeto será simplesmente copiado e convertido em uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="27848-132">If the object is not in a store, that is, if the byte count for the store record key passed in the  _cbStoreRecordKey_ parameter is zero, the object's entry identifier is simply copied and converted into a string.</span></span> 
  
<span data-ttu-id="27848-133">Chamar a função **HrComposeMsgID** é equivalente a chamar a função [HrComposeEID](hrcomposeeid.md) e, em seguida, a função [HrSzFromEntryID](hrszfromentryid.md) .</span><span class="sxs-lookup"><span data-stu-id="27848-133">Calling the **HrComposeMsgID** function is equivalent to calling the [HrComposeEID](hrcomposeeid.md) function and then the [HrSzFromEntryID](hrszfromentryid.md) function.</span></span> 
  
 <span data-ttu-id="27848-134">O **HrComposeMsgID** permite que os aplicativos cliente trabalhem com objetos em vários repositórios por meio do uso de identificadores de entrada compostos.</span><span class="sxs-lookup"><span data-stu-id="27848-134">**HrComposeMsgID** enables client applications to work with objects in multiple stores through the use of compound entry identifiers.</span></span> <span data-ttu-id="27848-135">Um aplicativo pode chamar a função [HrDecomposeMsgID](hrdecomposemsgid.md) para dividir o identificador de entrada composta em seus constituintes originais.</span><span class="sxs-lookup"><span data-stu-id="27848-135">An application can call the [HrDecomposeMsgID](hrdecomposemsgid.md) function to split the compound entry identifier into its original constituents.</span></span> 
  

