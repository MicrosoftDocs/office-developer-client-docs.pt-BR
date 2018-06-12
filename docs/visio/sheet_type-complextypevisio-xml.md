---
title: Sheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: f171f250fbe37ebf1d0d434709b06ab56804407f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772951"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="7702c-102">Sheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7702c-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7702c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="7702c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7702c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7702c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7702c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7702c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7702c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7702c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7702c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="7702c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7702c-108">None</span><span class="sxs-lookup"><span data-stu-id="7702c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7702c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7702c-109">Definition</span></span>

```XML
        <xs:complexType name="Sheet_Type" abstract="true">
        
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
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
    
    <xs:element name="Section"  type="Section_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs: name="" >
    </xs:>
    
      </xs:sequence>
    <xs:attribute name="LineStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="FillStyle"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TextStyle"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7702c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7702c-110">Elements and attributes</span></span>

<span data-ttu-id="7702c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7702c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7702c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7702c-112">Child elements</span></span>

|<span data-ttu-id="7702c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7702c-113">**Element**</span></span>|<span data-ttu-id="7702c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7702c-114">**Type**</span></span>|<span data-ttu-id="7702c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7702c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7702c-116">Célula</span><span class="sxs-lookup"><span data-stu-id="7702c-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="7702c-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7702c-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7702c-118">Seção</span><span class="sxs-lookup"><span data-stu-id="7702c-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7702c-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7702c-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7702c-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="7702c-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="7702c-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="7702c-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7702c-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="7702c-122">Attributes</span></span>

|<span data-ttu-id="7702c-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7702c-123">**Attribute**</span></span>|<span data-ttu-id="7702c-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7702c-124">**Type**</span></span>|<span data-ttu-id="7702c-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7702c-125">**Required**</span></span>|<span data-ttu-id="7702c-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7702c-126">**Description**</span></span>|<span data-ttu-id="7702c-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7702c-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7702c-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="7702c-128">FillStyle</span></span>  <br/> |<span data-ttu-id="7702c-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7702c-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7702c-130">opcional</span><span class="sxs-lookup"><span data-stu-id="7702c-130">optional</span></span>  <br/> ||<span data-ttu-id="7702c-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7702c-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7702c-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="7702c-132">LineStyle</span></span>  <br/> |<span data-ttu-id="7702c-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7702c-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7702c-134">opcional</span><span class="sxs-lookup"><span data-stu-id="7702c-134">optional</span></span>  <br/> ||<span data-ttu-id="7702c-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7702c-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7702c-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="7702c-136">TextStyle</span></span>  <br/> |<span data-ttu-id="7702c-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7702c-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7702c-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7702c-138">optional</span></span>  <br/> ||<span data-ttu-id="7702c-139">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7702c-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

