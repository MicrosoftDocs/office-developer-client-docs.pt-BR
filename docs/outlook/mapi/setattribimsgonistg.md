---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770382"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="202c9-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="202c9-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="202c9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="202c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="202c9-105">Define ou altera atributos das propriedades em um objeto [IMessage](imessageimapiprop.md) fornecido pela função [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="202c9-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="202c9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="202c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="202c9-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="202c9-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="202c9-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="202c9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="202c9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="202c9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="202c9-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="202c9-110">Called by:</span></span>  <br/> |<span data-ttu-id="202c9-111">Provedores de armazenamento de mensagens e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="202c9-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="202c9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="202c9-112">Parameters</span></span>

 <span data-ttu-id="202c9-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="202c9-113">_lpObject_</span></span>
  
> <span data-ttu-id="202c9-114">[in] Ponteiro para o objeto para o qual propriedade atributos estão sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="202c9-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="202c9-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="202c9-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="202c9-116">[in] Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) contendo uma matriz das marcas de propriedade indicando as propriedades para o qual propriedade atributos estão sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="202c9-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="202c9-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="202c9-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="202c9-118">[in] Ponteiro para uma estrutura [SPropAttrArray](spropattrarray.md) listando os atributos de propriedade para definir.</span><span class="sxs-lookup"><span data-stu-id="202c9-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="202c9-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="202c9-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="202c9-120">[out] Ponteiro para a estrutura de [SPropProblemArray](spropproblemarray.md) retornado contendo um conjunto de problemas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="202c9-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="202c9-121">Essa estrutura identifica os problemas encontrados se **SetAttribIMsgOnIStg** tiver sido apto a definir algumas propriedades, mas não todos.</span><span class="sxs-lookup"><span data-stu-id="202c9-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="202c9-122">Se o parâmetro _lppPropProblems_ é passado um ponteiro como NULL, nenhuma matriz de problema de propriedade é retornado, mesmo se algumas propriedades não foram definidas.</span><span class="sxs-lookup"><span data-stu-id="202c9-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="202c9-123">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="202c9-123">Return value</span></span>

<span data-ttu-id="202c9-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="202c9-124">S_OK</span></span> 
  
> <span data-ttu-id="202c9-125">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="202c9-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="202c9-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="202c9-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="202c9-127">Chamada bem-sucedida, mas uma ou mais propriedades não pôde ser acessadas e foram retornadas com um tipo de propriedade de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="202c9-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="202c9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="202c9-128">Remarks</span></span>

<span data-ttu-id="202c9-129">Atributos de propriedade só podem ser acessados na propriedade objetos, ou seja, objetos Implementando o [IMAPIProp: IUnknown](imapipropiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="202c9-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="202c9-130">Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um [IMessage: IMAPIProp](imessageimapiprop.md) objeto na parte superior do objeto OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="202c9-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="202c9-131">Os atributos de propriedade nesses objetos podem ser definidos ou alterados com **SetAttribIMsgOnIStg** e recuperados com [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="202c9-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="202c9-132">**Observação** **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os objetos **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="202c9-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="202c9-133">Eles só são válidos para **IMessage**- on - objetos **IStorage** retornados por **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="202c9-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="202c9-134">O parâmetro _lpPropAttrs_ , o número e a posição dos atributos devem coincidir com o número e a posição das marcas de propriedade passado no parâmetro _lpPropTags_ .</span><span class="sxs-lookup"><span data-stu-id="202c9-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="202c9-135">A função **SetAttribIMsgOnIStg** é usada para tornar as propriedades da mensagem somente leitura quando exigido pelo esquema **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="202c9-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="202c9-136">O provedor de armazenamento de mensagem de amostra usa-lo para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="202c9-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="202c9-137">Para obter mais informações, consulte [Messages](mapi-messages.md).</span><span class="sxs-lookup"><span data-stu-id="202c9-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

