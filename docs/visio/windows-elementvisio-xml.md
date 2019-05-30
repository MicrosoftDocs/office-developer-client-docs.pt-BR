---
title: Elemento do Windows (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1880734a-f086-ce6c-5a93-47851bcdd99d
description: Contém os elementos de janela de um documento.
ms.openlocfilehash: fcffcd5257b14c0ae0203a41f369536e583c1798
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538442"
---
# <a name="windows-element-visio-xml"></a><span data-ttu-id="234ea-103">Elemento do Windows (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="234ea-103">Windows element (Visio XML)</span></span>

<span data-ttu-id="234ea-104">Contém os elementos de **janela** de um documento.</span><span class="sxs-lookup"><span data-stu-id="234ea-104">Contains the **Window** elements for a document.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="234ea-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="234ea-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="234ea-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="234ea-106">**Element type**</span></span> <br/> |[<span data-ttu-id="234ea-107">Windows_Type</span><span class="sxs-lookup"><span data-stu-id="234ea-107">Windows_Type</span></span>](windows_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="234ea-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="234ea-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="234ea-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="234ea-109">**Schema file**</span></span> <br/> |<span data-ttu-id="234ea-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="234ea-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="234ea-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="234ea-111">**Document parts**</span></span> <br/> |<span data-ttu-id="234ea-112">Windows. xml</span><span class="sxs-lookup"><span data-stu-id="234ea-112">windows.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="234ea-113">Definição</span><span class="sxs-lookup"><span data-stu-id="234ea-113">Definition</span></span>

```XML
<xs:element name="Windows" type="Windows_Type" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="234ea-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="234ea-114">Elements and attributes</span></span>

<span data-ttu-id="234ea-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="234ea-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="234ea-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="234ea-116">Parent elements</span></span>

<span data-ttu-id="234ea-117">Nenhum</span><span class="sxs-lookup"><span data-stu-id="234ea-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="234ea-118">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="234ea-118">Child elements</span></span>

|<span data-ttu-id="234ea-119">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="234ea-119">**Element**</span></span>|<span data-ttu-id="234ea-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="234ea-120">**Type**</span></span>|<span data-ttu-id="234ea-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="234ea-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="234ea-122">Janela</span><span class="sxs-lookup"><span data-stu-id="234ea-122">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="234ea-123">Window_Type</span><span class="sxs-lookup"><span data-stu-id="234ea-123">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="234ea-124">Representa uma janela aberta em uma instância do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="234ea-124">Represents an open window in a Microsoft Visio instance.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="234ea-125">Atributos</span><span class="sxs-lookup"><span data-stu-id="234ea-125">Attributes</span></span>

|<span data-ttu-id="234ea-126">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="234ea-126">**Attribute**</span></span>|<span data-ttu-id="234ea-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="234ea-127">**Type**</span></span>|<span data-ttu-id="234ea-128">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="234ea-128">**Required**</span></span>|<span data-ttu-id="234ea-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="234ea-129">**Description**</span></span>|<span data-ttu-id="234ea-130">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="234ea-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="234ea-131">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="234ea-131">ClientHeight</span></span>  <br/> |<span data-ttu-id="234ea-132">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="234ea-132">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="234ea-133">opcional</span><span class="sxs-lookup"><span data-stu-id="234ea-133">optional</span></span>  <br/> |<span data-ttu-id="234ea-134">Representa a dimensão de altura de uma área de exibição</span><span class="sxs-lookup"><span data-stu-id="234ea-134">Represents the height dimension of a display area</span></span>  <br/> |<span data-ttu-id="234ea-135">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="234ea-135">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="234ea-136">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="234ea-136">ClientWidth</span></span>  <br/> |<span data-ttu-id="234ea-137">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="234ea-137">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="234ea-138">opcional</span><span class="sxs-lookup"><span data-stu-id="234ea-138">optional</span></span>  <br/> |<span data-ttu-id="234ea-139">Representa a dimensão de largura de uma área de exibição</span><span class="sxs-lookup"><span data-stu-id="234ea-139">Represents the width dimension of a display area</span></span>  <br/> |<span data-ttu-id="234ea-140">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="234ea-140">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

