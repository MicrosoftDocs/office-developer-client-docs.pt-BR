---
title: Row_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: d728363e6a3e7cd7fca2b95d91469f0d50ae1c39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538155"
---
# <a name="row_type-complextype-visio-xml"></a><span data-ttu-id="524b8-102">Row_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="524b8-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="524b8-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="524b8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="524b8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="524b8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="524b8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="524b8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="524b8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="524b8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="524b8-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="524b8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="524b8-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="524b8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="524b8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="524b8-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="524b8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="524b8-110">Elements and attributes</span></span>

<span data-ttu-id="524b8-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="524b8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="524b8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="524b8-112">Child elements</span></span>

|<span data-ttu-id="524b8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="524b8-113">**Element**</span></span>|<span data-ttu-id="524b8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="524b8-114">**Type**</span></span>|<span data-ttu-id="524b8-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="524b8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="524b8-116">Cell</span><span class="sxs-lookup"><span data-stu-id="524b8-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="524b8-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="524b8-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="524b8-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="524b8-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="524b8-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="524b8-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="524b8-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="524b8-120">Attributes</span></span>

|<span data-ttu-id="524b8-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="524b8-121">**Attribute**</span></span>|<span data-ttu-id="524b8-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="524b8-122">**Type**</span></span>|<span data-ttu-id="524b8-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="524b8-123">**Required**</span></span>|<span data-ttu-id="524b8-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="524b8-124">**Description**</span></span>|<span data-ttu-id="524b8-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="524b8-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="524b8-126">Del</span><span class="sxs-lookup"><span data-stu-id="524b8-126">Del</span></span>  <br/> |<span data-ttu-id="524b8-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="524b8-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="524b8-128">opcional</span><span class="sxs-lookup"><span data-stu-id="524b8-128">optional</span></span>  <br/> ||<span data-ttu-id="524b8-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="524b8-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="524b8-130">IX</span><span class="sxs-lookup"><span data-stu-id="524b8-130">IX</span></span>  <br/> |<span data-ttu-id="524b8-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="524b8-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="524b8-132">opcional</span><span class="sxs-lookup"><span data-stu-id="524b8-132">optional</span></span>  <br/> ||<span data-ttu-id="524b8-133">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="524b8-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="524b8-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="524b8-134">LocalName</span></span>  <br/> |<span data-ttu-id="524b8-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="524b8-135">xsd:string</span></span>  <br/> |<span data-ttu-id="524b8-136">opcional</span><span class="sxs-lookup"><span data-stu-id="524b8-136">optional</span></span>  <br/> ||<span data-ttu-id="524b8-137">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="524b8-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="524b8-138">N</span><span class="sxs-lookup"><span data-stu-id="524b8-138">N</span></span>  <br/> |<span data-ttu-id="524b8-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="524b8-139">xsd:string</span></span>  <br/> |<span data-ttu-id="524b8-140">opcional</span><span class="sxs-lookup"><span data-stu-id="524b8-140">optional</span></span>  <br/> ||<span data-ttu-id="524b8-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="524b8-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="524b8-142">T</span><span class="sxs-lookup"><span data-stu-id="524b8-142">T</span></span>  <br/> |<span data-ttu-id="524b8-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="524b8-143">xsd:string</span></span>  <br/> |<span data-ttu-id="524b8-144">opcional</span><span class="sxs-lookup"><span data-stu-id="524b8-144">optional</span></span>  <br/> ||<span data-ttu-id="524b8-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="524b8-145">Values of the xsd:string type.</span></span>  <br/> |
   

