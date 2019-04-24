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
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337965"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="6476b-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="6476b-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="6476b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6476b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6476b-105">Define ou altera atributos de propriedades em um objeto [IMessage](imessageimapiprop.md) fornecido pela função [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="6476b-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6476b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6476b-106">Header file:</span></span>  <br/> |<span data-ttu-id="6476b-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="6476b-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="6476b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6476b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6476b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6476b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6476b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6476b-110">Called by:</span></span>  <br/> |<span data-ttu-id="6476b-111">Provedores de repositórios de mensagens e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="6476b-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="6476b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6476b-112">Parameters</span></span>

 <span data-ttu-id="6476b-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="6476b-113">_lpObject_</span></span>
  
> <span data-ttu-id="6476b-114">no Ponteiro para o objeto para o qual os atributos de propriedade estão sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6476b-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="6476b-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="6476b-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="6476b-116">no Ponteiro para uma estrutura [SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades para as quais os atributos de propriedade estão sendo definidos.</span><span class="sxs-lookup"><span data-stu-id="6476b-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="6476b-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="6476b-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="6476b-118">no Ponteiro para uma estrutura [SPropAttrArray](spropattrarray.md) listando os atributos de propriedade a serem definidos.</span><span class="sxs-lookup"><span data-stu-id="6476b-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="6476b-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="6476b-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="6476b-120">bota Ponteiro para a estrutura [SPropProblemArray](spropproblemarray.md) retornada que contém um conjunto de problemas de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6476b-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="6476b-121">Esta estrutura identifica problemas encontrados se **SetAttribIMsgOnIStg** foi capaz de definir algumas propriedades, mas não todas.</span><span class="sxs-lookup"><span data-stu-id="6476b-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="6476b-122">Se um ponteiro para NULL for passado no parâmetro _lppPropProblems_ , nenhuma matriz de problemas de propriedade será retornada, mesmo que algumas propriedades não tenham sido definidas.</span><span class="sxs-lookup"><span data-stu-id="6476b-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6476b-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6476b-123">Return value</span></span>

<span data-ttu-id="6476b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="6476b-124">S_OK</span></span> 
  
> <span data-ttu-id="6476b-125">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="6476b-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6476b-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="6476b-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="6476b-127">A chamada foi bem-sucedida, mas uma ou mais propriedades não puderam ser acessadas e retornadas com um tipo de propriedade de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="6476b-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6476b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="6476b-128">Remarks</span></span>

<span data-ttu-id="6476b-129">Atributos de propriedade só podem ser acessados em objetos Property, ou seja, objetos que implementam a interface [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="6476b-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="6476b-130">Para disponibilizar as propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um objeto [IMessage: IMAPIProp](imessageimapiprop.md) na parte superior do objeto OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="6476b-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="6476b-131">Os atributos de propriedade desses objetos podem ser definidos ou alterados com **SetAttribIMsgOnIStg** e recuperados com o [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="6476b-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="6476b-132">**Observação** **GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os objetos **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="6476b-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="6476b-133">Eles são válidos apenas para objetos **IMessage**-on- **IStorage** retornados por **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="6476b-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="6476b-134">No parâmetro _lpPropAttrs_ , o número e a posição dos atributos devem corresponder ao número e à posição das marcas de propriedade passadas no parâmetro _lpPropTags_ .</span><span class="sxs-lookup"><span data-stu-id="6476b-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="6476b-135">A função **SetAttribIMsgOnIStg** é usada para tornar as propriedades de mensagem somente leitura quando exigidos pelo esquema **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="6476b-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="6476b-136">O exemplo de provedor de repositório de mensagens o utiliza para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="6476b-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="6476b-137">Para obter mais informações, [](mapi-messages.md)consulte messages.</span><span class="sxs-lookup"><span data-stu-id="6476b-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

