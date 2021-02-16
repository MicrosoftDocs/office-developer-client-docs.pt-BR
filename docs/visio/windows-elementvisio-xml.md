---
title: Elemento Windows (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contém os elementos Window de um documento.
ms.openlocfilehash: fcffcd5257b14c0ae0203a41f369536e583c1798
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538442"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="c98f0-103">Elemento Windows (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="c98f0-103">Windows element (Visio XML)</span></span>

<span data-ttu-id="c98f0-104">Contém os **elementos Window** de um documento.</span><span class="sxs-lookup"><span data-stu-id="c98f0-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c98f0-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="c98f0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c98f0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="c98f0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c98f0-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="c98f0-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c98f0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c98f0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c98f0-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c98f0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c98f0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c98f0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c98f0-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="c98f0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c98f0-112">windows.xml</span><span class="sxs-lookup"><span data-stu-id="c98f0-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c98f0-113">Definição</span><span class="sxs-lookup"><span data-stu-id="c98f0-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c98f0-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c98f0-114">Elements and attributes</span></span>

<span data-ttu-id="c98f0-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c98f0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c98f0-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="c98f0-116">Parent elements</span></span>

<span data-ttu-id="c98f0-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c98f0-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c98f0-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c98f0-118">Child elements</span></span>

|<span data-ttu-id="c98f0-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c98f0-119">**Element**</span></span>|<span data-ttu-id="c98f0-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c98f0-120">**Type**</span></span>|<span data-ttu-id="c98f0-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c98f0-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c98f0-122">Janela</span><span class="sxs-lookup"><span data-stu-id="c98f0-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c98f0-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="c98f0-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c98f0-124">Representa uma janela aberta em uma instância do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="c98f0-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c98f0-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="c98f0-125">Attributes</span></span>

|<span data-ttu-id="c98f0-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c98f0-126">**Attribute**</span></span>|<span data-ttu-id="c98f0-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c98f0-127">**Type**</span></span>|<span data-ttu-id="c98f0-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c98f0-128">**Required**</span></span>|<span data-ttu-id="c98f0-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c98f0-129">**Description**</span></span>|<span data-ttu-id="c98f0-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c98f0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c98f0-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="c98f0-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="c98f0-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c98f0-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c98f0-133">opcional</span><span class="sxs-lookup"><span data-stu-id="c98f0-133">optional</span></span>  <br/> |<span data-ttu-id="c98f0-134">Representa a dimensão de altura de uma área de exibição</span><span class="sxs-lookup"><span data-stu-id="c98f0-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="c98f0-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c98f0-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c98f0-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="c98f0-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="c98f0-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c98f0-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c98f0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="c98f0-138">optional</span></span>  <br/> |<span data-ttu-id="c98f0-139">Representa a dimensão de largura de uma área de exibição</span><span class="sxs-lookup"><span data-stu-id="c98f0-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="c98f0-140">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c98f0-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

