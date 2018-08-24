---
title: Section_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 71f94a84fe24fef4c5c9a55f59eec664982cd8a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594744"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="e0466-102">Section_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e0466-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="e0466-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="e0466-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0466-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e0466-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e0466-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="e0466-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e0466-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="e0466-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e0466-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="e0466-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e0466-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e0466-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e0466-109">Definição</span><span class="sxs-lookup"><span data-stu-id="e0466-109">Definition</span></span>

```XML
          <xs:complexType name="Section_Type">
          
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
    
    <xs:element name="Row"  type="Row_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e0466-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="e0466-110">Elements and attributes</span></span>

<span data-ttu-id="e0466-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="e0466-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e0466-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="e0466-112">Child elements</span></span>

|<span data-ttu-id="e0466-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e0466-113">**Element**</span></span>|<span data-ttu-id="e0466-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e0466-114">**Type**</span></span>|<span data-ttu-id="e0466-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e0466-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e0466-116">Célula</span><span class="sxs-lookup"><span data-stu-id="e0466-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="e0466-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="e0466-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0466-118">Row</span><span class="sxs-lookup"><span data-stu-id="e0466-118">Row</span></span>](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="e0466-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="e0466-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="e0466-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="e0466-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="e0466-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="e0466-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e0466-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="e0466-122">Attributes</span></span>

|<span data-ttu-id="e0466-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="e0466-123">**Attribute**</span></span>|<span data-ttu-id="e0466-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e0466-124">**Type**</span></span>|<span data-ttu-id="e0466-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="e0466-125">**Required**</span></span>|<span data-ttu-id="e0466-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e0466-126">**Description**</span></span>|<span data-ttu-id="e0466-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="e0466-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e0466-128">DEL</span><span class="sxs-lookup"><span data-stu-id="e0466-128">Del</span></span>  <br/> |<span data-ttu-id="e0466-129">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="e0466-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="e0466-130">opcional</span><span class="sxs-lookup"><span data-stu-id="e0466-130">optional</span></span>  <br/> ||<span data-ttu-id="e0466-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="e0466-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="e0466-132">IX</span><span class="sxs-lookup"><span data-stu-id="e0466-132">IX</span></span>  <br/> |<span data-ttu-id="e0466-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e0466-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e0466-134">opcional</span><span class="sxs-lookup"><span data-stu-id="e0466-134">optional</span></span>  <br/> ||<span data-ttu-id="e0466-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e0466-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e0466-136">N</span><span class="sxs-lookup"><span data-stu-id="e0466-136">N</span></span>  <br/> |<span data-ttu-id="e0466-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="e0466-137">xsd:string</span></span>  <br/> |<span data-ttu-id="e0466-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="e0466-138">required</span></span>  <br/> ||<span data-ttu-id="e0466-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e0466-139">Values of the xsd:string type.</span></span>  <br/> |
   

