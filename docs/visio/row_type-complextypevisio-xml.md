---
title: Row_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: 6ebd483ae9b0748a3afa15360bf2c88feae44aeb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586897"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="b6289-102">Row_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b6289-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b6289-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="b6289-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b6289-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b6289-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b6289-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b6289-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b6289-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b6289-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b6289-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="b6289-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b6289-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6289-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b6289-109">Definição</span><span class="sxs-lookup"><span data-stu-id="b6289-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b6289-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b6289-110">Elements and attributes</span></span>

<span data-ttu-id="b6289-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b6289-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b6289-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b6289-112">Child elements</span></span>

|<span data-ttu-id="b6289-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b6289-113">**Element**</span></span>|<span data-ttu-id="b6289-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b6289-114">**Type**</span></span>|<span data-ttu-id="b6289-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b6289-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b6289-116">Célula</span><span class="sxs-lookup"><span data-stu-id="b6289-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="b6289-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="b6289-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="b6289-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="b6289-118">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="b6289-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="b6289-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b6289-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="b6289-120">Attributes</span></span>

|<span data-ttu-id="b6289-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b6289-121">**Attribute**</span></span>|<span data-ttu-id="b6289-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b6289-122">**Type**</span></span>|<span data-ttu-id="b6289-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b6289-123">**Required**</span></span>|<span data-ttu-id="b6289-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b6289-124">**Description**</span></span>|<span data-ttu-id="b6289-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="b6289-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b6289-126">DEL</span><span class="sxs-lookup"><span data-stu-id="b6289-126">Del</span></span>  <br/> |<span data-ttu-id="b6289-127">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="b6289-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b6289-128">opcional</span><span class="sxs-lookup"><span data-stu-id="b6289-128">optional</span></span>  <br/> ||<span data-ttu-id="b6289-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b6289-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b6289-130">IX</span><span class="sxs-lookup"><span data-stu-id="b6289-130">IX</span></span>  <br/> |<span data-ttu-id="b6289-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b6289-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b6289-132">opcional</span><span class="sxs-lookup"><span data-stu-id="b6289-132">optional</span></span>  <br/> ||<span data-ttu-id="b6289-133">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b6289-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b6289-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="b6289-134">LocalName</span></span>  <br/> |<span data-ttu-id="b6289-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b6289-135">xsd:string</span></span>  <br/> |<span data-ttu-id="b6289-136">opcional</span><span class="sxs-lookup"><span data-stu-id="b6289-136">optional</span></span>  <br/> ||<span data-ttu-id="b6289-137">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b6289-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b6289-138">N</span><span class="sxs-lookup"><span data-stu-id="b6289-138">N</span></span>  <br/> |<span data-ttu-id="b6289-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b6289-139">xsd:string</span></span>  <br/> |<span data-ttu-id="b6289-140">opcional</span><span class="sxs-lookup"><span data-stu-id="b6289-140">optional</span></span>  <br/> ||<span data-ttu-id="b6289-141">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b6289-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="b6289-142">T</span><span class="sxs-lookup"><span data-stu-id="b6289-142">T</span></span>  <br/> |<span data-ttu-id="b6289-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="b6289-143">xsd:string</span></span>  <br/> |<span data-ttu-id="b6289-144">opcional</span><span class="sxs-lookup"><span data-stu-id="b6289-144">optional</span></span>  <br/> ||<span data-ttu-id="b6289-145">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="b6289-145">Values of the xsd:string type.</span></span>  <br/> |
   

