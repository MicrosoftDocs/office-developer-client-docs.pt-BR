---
title: Constantes (Outlook exportados APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tópico contém definições constantes para APIs que exporta do Outlook.
ms.openlocfilehash: 54b491e436b7b9275a227de40439ddb66d8d0c5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765796"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="4742b-103">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="4742b-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="4742b-104">Este tópico contém definições constantes para APIs que exporta do Outlook.</span><span class="sxs-lookup"><span data-stu-id="4742b-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="4742b-105">Definições para suporte de fuso horário</span><span class="sxs-lookup"><span data-stu-id="4742b-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="4742b-106">Definições para suporte de categoria</span><span class="sxs-lookup"><span data-stu-id="4742b-106">Definitions for Category support</span></span>

|<span data-ttu-id="4742b-107">**Constante**</span><span class="sxs-lookup"><span data-stu-id="4742b-107">**Constant**</span></span>|<span data-ttu-id="4742b-108">**Definição**</span><span class="sxs-lookup"><span data-stu-id="4742b-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4742b-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="4742b-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="4742b-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4742b-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="4742b-111">Identificadores de expedição Miscellaneous</span><span class="sxs-lookup"><span data-stu-id="4742b-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="4742b-112">Outlook expõe os seguintes identificadores de expedição (dispids) para que os desenvolvedores podem usar [IDispatch:: Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) para acessar o método ou a propriedade correspondente ou ouvir o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="4742b-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](http://msdn.microsoft.com/library/automat.idispatch_invoke%28Office.15%29.aspx) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="4742b-113">**Constante associada**</span><span class="sxs-lookup"><span data-stu-id="4742b-113">**Associated constant**</span></span>|<span data-ttu-id="4742b-114">**Valor DISPID**</span><span class="sxs-lookup"><span data-stu-id="4742b-114">**Dispid value**</span></span>|<span data-ttu-id="4742b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4742b-115">**Description**</span></span>|<span data-ttu-id="4742b-116">**Interface aplicável**</span><span class="sxs-lookup"><span data-stu-id="4742b-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4742b-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="4742b-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="4742b-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="4742b-118">0xF024</span></span>  <br/> |<span data-ttu-id="4742b-119">Usado para chamar a propriedade correspondente em um item para verificar se o item foi modificado, mas não foi salvo.</span><span class="sxs-lookup"><span data-stu-id="4742b-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="4742b-120">Objetos de nível de item</span><span class="sxs-lookup"><span data-stu-id="4742b-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="4742b-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="4742b-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="4742b-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="4742b-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="4742b-123">Usado para chamar o método correspondente no explorer ou inspector para especificar se deseja exibir a imagem de um contato, com base em um determinado argumento.</span><span class="sxs-lookup"><span data-stu-id="4742b-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="4742b-124">Explorer ou inspector</span><span class="sxs-lookup"><span data-stu-id="4742b-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="4742b-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="4742b-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="4742b-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="4742b-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="4742b-127">Usado para manipular o evento a partir da função **IDispatch:: Invoke** que é acionado antes de uma operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="4742b-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="4742b-128">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4742b-128">Application</span></span>  <br/> |
|<span data-ttu-id="4742b-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="4742b-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="4742b-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="4742b-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="4742b-131">Usado para manipular o evento a partir da função **IDispatch:: Invoke** que é acionado quando o Outlook concluiu a ler as propriedades do item.</span><span class="sxs-lookup"><span data-stu-id="4742b-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="4742b-132">Objetos de nível de item</span><span class="sxs-lookup"><span data-stu-id="4742b-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4742b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="4742b-133">See also</span></span>

- [<span data-ttu-id="4742b-134">APIs de exportadas do Outlook</span><span class="sxs-lookup"><span data-stu-id="4742b-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="4742b-135">Sobre APIs exportado pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="4742b-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="4742b-136">Determinar se um item do Outlook foi modificado, mas não salvo (referência auxiliar do Outlook)</span><span class="sxs-lookup"><span data-stu-id="4742b-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="4742b-137">Especifique se deseja exibir a imagem de um contato no Outlook (referência auxiliar do Outlook)</span><span class="sxs-lookup"><span data-stu-id="4742b-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/pt-br/library/office/gg262879.aspx)
- [<span data-ttu-id="4742b-138">Eventos disponíveis e os dispids (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="4742b-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

