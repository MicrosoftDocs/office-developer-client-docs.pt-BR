---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439993"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="c72a2-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="c72a2-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="c72a2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c72a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c72a2-105">Recupera atributos de propriedades em um [objeto IMessage](imessageimapiprop.md) fornecido pela [função OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="c72a2-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c72a2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c72a2-106">Header file:</span></span>  <br/> |<span data-ttu-id="c72a2-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="c72a2-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="c72a2-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c72a2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c72a2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c72a2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c72a2-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c72a2-110">Called by:</span></span>  <br/> |<span data-ttu-id="c72a2-111">Aplicativos cliente e provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="c72a2-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="c72a2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c72a2-112">Parameters</span></span>

 <span data-ttu-id="c72a2-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="c72a2-113">_lpObject_</span></span>
  
> <span data-ttu-id="c72a2-114">[in] Ponteiro para um **objeto IMessage** obtido da [função OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="c72a2-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="c72a2-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="c72a2-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="c72a2-116">[in] Ponteiro para uma [estrutura SPropTagArray](sproptagarray.md) que contém uma matriz de marcas de propriedade indicando as propriedades para as quais os atributos devem ser recuperados.</span><span class="sxs-lookup"><span data-stu-id="c72a2-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="c72a2-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="c72a2-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="c72a2-118">[out] Ponteiro para um ponteiro para a [estrutura SPropAttrArray](spropattrarray.md) retornada que contém os atributos de propriedade recuperados.</span><span class="sxs-lookup"><span data-stu-id="c72a2-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c72a2-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c72a2-119">Return value</span></span>

<span data-ttu-id="c72a2-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="c72a2-120">S_OK</span></span> 
  
> <span data-ttu-id="c72a2-121">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c72a2-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="c72a2-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="c72a2-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="c72a2-123">A chamada foi bem-sucedida em geral, mas uma ou mais propriedades não puderam ser acessadas e foram retornadas com um tipo de propriedade de PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="c72a2-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c72a2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c72a2-124">Remarks</span></span>

<span data-ttu-id="c72a2-125">Atributos de propriedade só podem ser acessados em objetos de propriedade, ou seja, objetos que implementam o [IMAPIProp : interface IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="c72a2-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="c72a2-126">Para disponibilizar propriedades MAPI em um objeto de armazenamento estruturado OLE, [OpenIMsgOnIStg](openimsgonistg.md) cria um [IMessage : objeto IMAPIProp](imessageimapiprop.md) sobre o objeto **IStorage** OLE.</span><span class="sxs-lookup"><span data-stu-id="c72a2-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="c72a2-127">Os atributos de propriedade nesses objetos podem ser definidos ou alterados com [SetAttribIMsgOnIStg](setattribimsgonistg.md) e recuperados com **GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="c72a2-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c72a2-128">**GetAttribIMsgOnIStg** e **SetAttribIMsgOnIStg** não operam em todos os **objetos IMessage.**</span><span class="sxs-lookup"><span data-stu-id="c72a2-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="c72a2-129">Eles só são **válidos para objetos IMessage**-on-IStorage retornados por **OpenIMsgOnIStg**. </span><span class="sxs-lookup"><span data-stu-id="c72a2-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="c72a2-130">O número e as posições dos atributos no parâmetro _lppPropAttrArray_ correspondem ao número e às posições das marcas de propriedade no parâmetro _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="c72a2-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

