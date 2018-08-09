---
title: Elemento do Windows ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contém os elementos de janela para um documento.
ms.openlocfilehash: 70746ccfa2d99a9fdd5b3a91320c9372aa233c7a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773280"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="21be7-103">Elemento do Windows ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="21be7-103">Windows element ('Visio XML')</span></span>

<span data-ttu-id="21be7-104">Contém os elementos de **janela** para um documento.</span><span class="sxs-lookup"><span data-stu-id="21be7-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="21be7-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="21be7-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="21be7-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="21be7-106">**Element type**</span></span> <br/> |[<span data-ttu-id="21be7-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="21be7-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="21be7-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="21be7-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="21be7-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="21be7-109">**Schema file**</span></span> <br/> |<span data-ttu-id="21be7-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="21be7-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="21be7-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="21be7-111">**Document parts**</span></span> <br/> |<span data-ttu-id="21be7-112">Windows.XML</span><span class="sxs-lookup"><span data-stu-id="21be7-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="21be7-113">Definição</span><span class="sxs-lookup"><span data-stu-id="21be7-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="21be7-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="21be7-114">Elements and attributes</span></span>

<span data-ttu-id="21be7-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="21be7-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="21be7-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="21be7-116">Parent elements</span></span>

<span data-ttu-id="21be7-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="21be7-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="21be7-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="21be7-118">Child elements</span></span>

|<span data-ttu-id="21be7-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="21be7-119">**Element**</span></span>|<span data-ttu-id="21be7-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="21be7-120">**Type**</span></span>|<span data-ttu-id="21be7-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="21be7-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="21be7-122">Window</span><span class="sxs-lookup"><span data-stu-id="21be7-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="21be7-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="21be7-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="21be7-124">Representa uma janela aberta em uma estância do Microsoft Visio.
</span><span class="sxs-lookup"><span data-stu-id="21be7-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="21be7-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="21be7-125">Attributes</span></span>

|<span data-ttu-id="21be7-126">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="21be7-126">**Attribute**</span></span>|<span data-ttu-id="21be7-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="21be7-127">**Type**</span></span>|<span data-ttu-id="21be7-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="21be7-128">**Required**</span></span>|<span data-ttu-id="21be7-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="21be7-129">**Description**</span></span>|<span data-ttu-id="21be7-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="21be7-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="21be7-131">Propriedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="21be7-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="21be7-132">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="21be7-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="21be7-133">opcional</span><span class="sxs-lookup"><span data-stu-id="21be7-133">optional</span></span>  <br/> |<span data-ttu-id="21be7-134">Representa a dimensão de altura de uma área de exibição</span><span class="sxs-lookup"><span data-stu-id="21be7-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="21be7-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="21be7-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="21be7-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="21be7-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="21be7-137">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="21be7-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="21be7-138">opcional</span><span class="sxs-lookup"><span data-stu-id="21be7-138">optional</span></span>  <br/> |<span data-ttu-id="21be7-139">Representa a dimensão de largura de uma área de exibição</span><span class="sxs-lookup"><span data-stu-id="21be7-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="21be7-140">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="21be7-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

