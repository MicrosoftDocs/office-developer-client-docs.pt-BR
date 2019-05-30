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
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="3e2cf-102">Row_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="3e2cf-102">Row_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="3e2cf-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="3e2cf-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e2cf-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3e2cf-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3e2cf-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3e2cf-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3e2cf-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3e2cf-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3e2cf-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3e2cf-109">Definição</span><span class="sxs-lookup"><span data-stu-id="3e2cf-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3e2cf-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="3e2cf-110">Elements and attributes</span></span>

<span data-ttu-id="3e2cf-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="3e2cf-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3e2cf-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="3e2cf-112">Child elements</span></span>

|<span data-ttu-id="3e2cf-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-113">**Element**</span></span>|<span data-ttu-id="3e2cf-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-114">**Type**</span></span>|<span data-ttu-id="3e2cf-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3e2cf-116">Cell</span><span class="sxs-lookup"><span data-stu-id="3e2cf-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="3e2cf-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="3e2cf-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="3e2cf-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="3e2cf-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="3e2cf-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="3e2cf-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3e2cf-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="3e2cf-120">Attributes</span></span>

|<span data-ttu-id="3e2cf-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-121">**Attribute**</span></span>|<span data-ttu-id="3e2cf-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-122">**Type**</span></span>|<span data-ttu-id="3e2cf-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-123">**Required**</span></span>|<span data-ttu-id="3e2cf-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-124">**Description**</span></span>|<span data-ttu-id="3e2cf-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="3e2cf-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3e2cf-126">Del</span><span class="sxs-lookup"><span data-stu-id="3e2cf-126">Del</span></span>  <br/> |<span data-ttu-id="3e2cf-127">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="3e2cf-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3e2cf-128">opcional</span><span class="sxs-lookup"><span data-stu-id="3e2cf-128">optional</span></span>  <br/> ||<span data-ttu-id="3e2cf-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="3e2cf-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3e2cf-130">IX</span><span class="sxs-lookup"><span data-stu-id="3e2cf-130">IX</span></span>  <br/> |<span data-ttu-id="3e2cf-131">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="3e2cf-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="3e2cf-132">opcional</span><span class="sxs-lookup"><span data-stu-id="3e2cf-132">optional</span></span>  <br/> ||<span data-ttu-id="3e2cf-133">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="3e2cf-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="3e2cf-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="3e2cf-134">LocalName</span></span>  <br/> |<span data-ttu-id="3e2cf-135">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3e2cf-135">xsd:string</span></span>  <br/> |<span data-ttu-id="3e2cf-136">opcional</span><span class="sxs-lookup"><span data-stu-id="3e2cf-136">optional</span></span>  <br/> ||<span data-ttu-id="3e2cf-137">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3e2cf-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e2cf-138">N</span><span class="sxs-lookup"><span data-stu-id="3e2cf-138">N</span></span>  <br/> |<span data-ttu-id="3e2cf-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3e2cf-139">xsd:string</span></span>  <br/> |<span data-ttu-id="3e2cf-140">opcional</span><span class="sxs-lookup"><span data-stu-id="3e2cf-140">optional</span></span>  <br/> ||<span data-ttu-id="3e2cf-141">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3e2cf-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="3e2cf-142">T</span><span class="sxs-lookup"><span data-stu-id="3e2cf-142">T</span></span>  <br/> |<span data-ttu-id="3e2cf-143">xsd:string</span><span class="sxs-lookup"><span data-stu-id="3e2cf-143">xsd:string</span></span>  <br/> |<span data-ttu-id="3e2cf-144">opcional</span><span class="sxs-lookup"><span data-stu-id="3e2cf-144">optional</span></span>  <br/> ||<span data-ttu-id="3e2cf-145">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="3e2cf-145">Values of the xsd:string type.</span></span>  <br/> |
   

