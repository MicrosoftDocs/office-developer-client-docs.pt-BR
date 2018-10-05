---
title: Section_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 35cd638d36f4ddd1d90e0c312e65626f7d8b0bff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384294"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="2280e-102">Section_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="2280e-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2280e-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="2280e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2280e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="2280e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2280e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="2280e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2280e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2280e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2280e-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="2280e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2280e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="2280e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2280e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="2280e-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2280e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="2280e-110">Elements and attributes</span></span>

<span data-ttu-id="2280e-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="2280e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2280e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="2280e-112">Child elements</span></span>

|<span data-ttu-id="2280e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2280e-113">**Element**</span></span>|<span data-ttu-id="2280e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2280e-114">**Type**</span></span>|<span data-ttu-id="2280e-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2280e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2280e-116">Célula</span><span class="sxs-lookup"><span data-stu-id="2280e-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="2280e-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="2280e-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2280e-118">Row</span><span class="sxs-lookup"><span data-stu-id="2280e-118">Row</span></span>](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="2280e-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="2280e-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="2280e-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="2280e-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="2280e-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="2280e-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2280e-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="2280e-122">Attributes</span></span>

|<span data-ttu-id="2280e-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="2280e-123">**Attribute**</span></span>|<span data-ttu-id="2280e-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="2280e-124">**Type**</span></span>|<span data-ttu-id="2280e-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="2280e-125">**Required**</span></span>|<span data-ttu-id="2280e-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2280e-126">**Description**</span></span>|<span data-ttu-id="2280e-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="2280e-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2280e-128">DEL</span><span class="sxs-lookup"><span data-stu-id="2280e-128">Del</span></span>  <br/> |<span data-ttu-id="2280e-129">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="2280e-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="2280e-130">opcional</span><span class="sxs-lookup"><span data-stu-id="2280e-130">optional</span></span>  <br/> ||<span data-ttu-id="2280e-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="2280e-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="2280e-132">IX</span><span class="sxs-lookup"><span data-stu-id="2280e-132">IX</span></span>  <br/> |<span data-ttu-id="2280e-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="2280e-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="2280e-134">opcional</span><span class="sxs-lookup"><span data-stu-id="2280e-134">optional</span></span>  <br/> ||<span data-ttu-id="2280e-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="2280e-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="2280e-136">N</span><span class="sxs-lookup"><span data-stu-id="2280e-136">N</span></span>  <br/> |<span data-ttu-id="2280e-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="2280e-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2280e-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="2280e-138">required</span></span>  <br/> ||<span data-ttu-id="2280e-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="2280e-139">Values of the xsd:string type.</span></span>  <br/> |
   

