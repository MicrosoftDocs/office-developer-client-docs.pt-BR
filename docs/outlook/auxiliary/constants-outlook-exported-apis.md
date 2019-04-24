---
title: Constantes (Outlook exportados APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 7590a30e-3fd8-7ae3-f077-c80f6cc21d7b
description: Este tópico contém definições constantes para APIs exportadas pelo Outlook.
ms.openlocfilehash: 65181932b858da1b32c3fbe5fd0bd7e92ca8dc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319870"
---
# <a name="constants-outlook-exported-apis"></a><span data-ttu-id="d427d-103">Constantes (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="d427d-103">Constants (Outlook exported APIs)</span></span>

<span data-ttu-id="d427d-104">Este tópico contém definições constantes para APIs exportadas pelo Outlook.</span><span class="sxs-lookup"><span data-stu-id="d427d-104">This topic contains constant definitions for APIs that Outlook exports.</span></span>
  
## <a name="definitions-for-time-zone-support"></a><span data-ttu-id="d427d-105">Definições para suporte de fuso horário</span><span class="sxs-lookup"><span data-stu-id="d427d-105">Definitions for Time Zone support</span></span>

```cpp
const ULONG TZ_MAX_RULES                    = 0x00000001;  
const BYTE  TZ_BIN_VERSION_MAJOR            = 0x02;  
const BYTE  TZ_BIN_VERSION_MINOR            = 0x01; 
const WORD  TZRULE_FLAG_RECUR_CURRENT_TZREG = 0x0001; 
const WORD  TZRULE_FLAG_EFFECTIVE_TZREG     = 0x0002; 
const WORD  TZDEFINITION_FLAG_VALID_KEYNAME = 0x0002;
```

## <a name="definitions-for-category-support"></a><span data-ttu-id="d427d-106">Definições para suporte a categorias</span><span class="sxs-lookup"><span data-stu-id="d427d-106">Definitions for Category support</span></span>

|<span data-ttu-id="d427d-107">**Constante**</span><span class="sxs-lookup"><span data-stu-id="d427d-107">**Constant**</span></span>|<span data-ttu-id="d427d-108">**Definição**</span><span class="sxs-lookup"><span data-stu-id="d427d-108">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d427d-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="d427d-109">PCAFSIF_MSGEID_IS_SEARCH_KEY</span></span>  <br/> |<span data-ttu-id="d427d-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d427d-110">0x00000001</span></span>  <br/> |
   
## <a name="miscellaneous-dispatch-identifiers"></a><span data-ttu-id="d427d-111">Identificadores de expedição diversos</span><span class="sxs-lookup"><span data-stu-id="d427d-111">Miscellaneous dispatch identifiers</span></span>

<span data-ttu-id="d427d-112">O Outlook expõe os seguintes identificadores de expedição (DispIds) para que os desenvolvedores possam usar o [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) para acessar a propriedade ou o método correspondente ou ouvir o evento correspondente.</span><span class="sxs-lookup"><span data-stu-id="d427d-112">Outlook exposes the following dispatch identifiers (dispids) so that developers can use [IDispatch::Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) to access the corresponding property or method, or listen to the corresponding event.</span></span> 
  
|<span data-ttu-id="d427d-113">**Constante associada**</span><span class="sxs-lookup"><span data-stu-id="d427d-113">**Associated constant**</span></span>|<span data-ttu-id="d427d-114">**Valor de DISPID**</span><span class="sxs-lookup"><span data-stu-id="d427d-114">**Dispid value**</span></span>|<span data-ttu-id="d427d-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d427d-115">**Description**</span></span>|<span data-ttu-id="d427d-116">**Interface aplicável**</span><span class="sxs-lookup"><span data-stu-id="d427d-116">**Applicable interface**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d427d-117">**dispidFDirty**</span><span class="sxs-lookup"><span data-stu-id="d427d-117">**dispidFDirty**</span></span> <br/> |<span data-ttu-id="d427d-118">0xF024</span><span class="sxs-lookup"><span data-stu-id="d427d-118">0xF024</span></span>  <br/> |<span data-ttu-id="d427d-119">Usado para invocar a propriedade correspondente em um item para verificar se o item foi modificado, mas não foi salvo.</span><span class="sxs-lookup"><span data-stu-id="d427d-119">Used to invoke the corresponding property on an item to verify whether the item has been modified but has not been saved.</span></span>  <br/> |<span data-ttu-id="d427d-120">Objetos de nível de item</span><span class="sxs-lookup"><span data-stu-id="d427d-120">Item-level objects</span></span>  <br/> |
|<span data-ttu-id="d427d-121">**dispidShowSenderPhoto**</span><span class="sxs-lookup"><span data-stu-id="d427d-121">**dispidShowSenderPhoto**</span></span> <br/> |<span data-ttu-id="d427d-122">0xF0D0</span><span class="sxs-lookup"><span data-stu-id="d427d-122">0xF0D0</span></span>  <br/> |<span data-ttu-id="d427d-123">Usado para invocar o método correspondente no Explorer ou no Inspetor para especificar se deseja exibir a imagem de um contato, com base em um determinado argumento.</span><span class="sxs-lookup"><span data-stu-id="d427d-123">Used to invoke the corresponding method on the explorer or inspector to specify whether to display a contact's picture, based on a given argument.</span></span>  <br/> |<span data-ttu-id="d427d-124">Explorer ou Inspetor</span><span class="sxs-lookup"><span data-stu-id="d427d-124">Explorer or inspector</span></span>  <br/> |
|<span data-ttu-id="d427d-125">**dispidBeforePrint**</span><span class="sxs-lookup"><span data-stu-id="d427d-125">**dispidBeforePrint**</span></span> <br/> |<span data-ttu-id="d427d-126">0xFC8E</span><span class="sxs-lookup"><span data-stu-id="d427d-126">0xFC8E</span></span>  <br/> |<span data-ttu-id="d427d-127">Usado para manipular o evento da função **IDispatch:: Invoke** que é acionada antes de uma operação de impressão.</span><span class="sxs-lookup"><span data-stu-id="d427d-127">Used to handle the event from the **IDispatch::Invoke** function that fires before a printing operation.</span></span>  <br/> |<span data-ttu-id="d427d-128">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="d427d-128">Application</span></span>  <br/> |
|<span data-ttu-id="d427d-129">**dispidEventReadComplete**</span><span class="sxs-lookup"><span data-stu-id="d427d-129">**dispidEventReadComplete**</span></span> <br/> |<span data-ttu-id="d427d-130">0xFC8F</span><span class="sxs-lookup"><span data-stu-id="d427d-130">0xFC8F</span></span>  <br/> |<span data-ttu-id="d427d-131">Usado para manipular o evento da função **IDispatch:: Invoke** que é acionada quando o Outlook conclui a leitura das propriedades do item.</span><span class="sxs-lookup"><span data-stu-id="d427d-131">Used to handle the event from the **IDispatch::Invoke** function that fires when Outlook has completed reading the properties of the item.</span></span>  <br/> |<span data-ttu-id="d427d-132">Objetos de nível de item</span><span class="sxs-lookup"><span data-stu-id="d427d-132">Item-level objects</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d427d-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d427d-133">See also</span></span>

- [<span data-ttu-id="d427d-134">APIs exportadas do Outlook</span><span class="sxs-lookup"><span data-stu-id="d427d-134">Outlook exported APIs</span></span>](outlook-exported-apis.md)
- [<span data-ttu-id="d427d-135">Sobre APIs exportadas pelo Outlook</span><span class="sxs-lookup"><span data-stu-id="d427d-135">About APIs exported by Outlook</span></span>](about-apis-exported-by-outlook.md)
- [<span data-ttu-id="d427d-136">Determinar se um item do Outlook foi modificado, mas não salvo (referência do Outlook auxiliar)</span><span class="sxs-lookup"><span data-stu-id="d427d-136">Determine whether an Outlook item has been modified but not saved (Outlook Auxiliary Reference)</span></span>](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
- [<span data-ttu-id="d427d-137">Especificar se deseja exibir a imagem de um contato no Outlook (referência auxiliar do Outlook)</span><span class="sxs-lookup"><span data-stu-id="d427d-137">Specify whether to display a contact's picture in Outlook (Outlook Auxiliary Reference)</span></span>](https://msdn.microsoft.com/library/office/gg262879.aspx)
- [<span data-ttu-id="d427d-138">Eventos disponíveis e os dispids (Outlook exportados APIs)</span><span class="sxs-lookup"><span data-stu-id="d427d-138">Available events and their dispids (Outlook exported APIs)</span></span>](available-events-and-their-dispids-outlook-exported-apis.md)

