---
title: Sheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4855350c-8204-ef1f-4d08-4ab6540249e9
ms.openlocfilehash: dc8930ffa89baf059074a12bb285e6b53e329e41
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388746"
---
# <a name="sheettype-complextype-visio-xml"></a><span data-ttu-id="7086b-102">Sheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7086b-102">Sheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7086b-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="7086b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7086b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7086b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7086b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="7086b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7086b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7086b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7086b-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="7086b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7086b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="7086b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7086b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="7086b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7086b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="7086b-110">Elements and attributes</span></span>

<span data-ttu-id="7086b-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="7086b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7086b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="7086b-112">Child elements</span></span>

|<span data-ttu-id="7086b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7086b-113">**Element**</span></span>|<span data-ttu-id="7086b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7086b-114">**Type**</span></span>|<span data-ttu-id="7086b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7086b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7086b-116">Célula</span><span class="sxs-lookup"><span data-stu-id="7086b-116">Cell</span></span>](cell-elementvisio-xml.md) <br/> |[<span data-ttu-id="7086b-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="7086b-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7086b-118">Seção</span><span class="sxs-lookup"><span data-stu-id="7086b-118">Section</span></span>](section-element-sheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7086b-119">Section_Type</span><span class="sxs-lookup"><span data-stu-id="7086b-119">Section_Type</span></span>](section_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7086b-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="7086b-120">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="7086b-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="7086b-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7086b-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="7086b-122">Attributes</span></span>

|<span data-ttu-id="7086b-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="7086b-123">**Attribute**</span></span>|<span data-ttu-id="7086b-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="7086b-124">**Type**</span></span>|<span data-ttu-id="7086b-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="7086b-125">**Required**</span></span>|<span data-ttu-id="7086b-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7086b-126">**Description**</span></span>|<span data-ttu-id="7086b-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="7086b-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7086b-128">FillStyle</span><span class="sxs-lookup"><span data-stu-id="7086b-128">FillStyle</span></span>  <br/> |<span data-ttu-id="7086b-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7086b-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7086b-130">opcional</span><span class="sxs-lookup"><span data-stu-id="7086b-130">optional</span></span>  <br/> ||<span data-ttu-id="7086b-131">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7086b-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7086b-132">LineStyle</span><span class="sxs-lookup"><span data-stu-id="7086b-132">LineStyle</span></span>  <br/> |<span data-ttu-id="7086b-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7086b-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7086b-134">opcional</span><span class="sxs-lookup"><span data-stu-id="7086b-134">optional</span></span>  <br/> ||<span data-ttu-id="7086b-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7086b-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7086b-136">TextStyle</span><span class="sxs-lookup"><span data-stu-id="7086b-136">TextStyle</span></span>  <br/> |<span data-ttu-id="7086b-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7086b-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7086b-138">opcional</span><span class="sxs-lookup"><span data-stu-id="7086b-138">optional</span></span>  <br/> ||<span data-ttu-id="7086b-139">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7086b-139">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

