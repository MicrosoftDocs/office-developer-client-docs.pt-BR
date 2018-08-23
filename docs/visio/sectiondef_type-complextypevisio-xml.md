---
title: SectionDef_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: cd85dd97a8de7bc9a9ca34fd19669dd294fe6905
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589753"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="4ed49-102">SectionDef_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4ed49-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4ed49-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="4ed49-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ed49-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4ed49-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4ed49-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4ed49-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4ed49-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4ed49-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4ed49-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="4ed49-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4ed49-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4ed49-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4ed49-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4ed49-109">Definition</span></span>

```XML
          <xs:complexType name="SectionDef_Type">
          
          <xs:sequence>
    <xs:element name="CellDef"  type="CellDef_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowDef"  type="RowDef_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="S"
  type="xsd:unsignedByte"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4ed49-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4ed49-110">Elements and attributes</span></span>

<span data-ttu-id="4ed49-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4ed49-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4ed49-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4ed49-112">Child elements</span></span>

|<span data-ttu-id="4ed49-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4ed49-113">**Element**</span></span>|<span data-ttu-id="4ed49-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4ed49-114">**Type**</span></span>|<span data-ttu-id="4ed49-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4ed49-115">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4ed49-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="4ed49-116">CellDef</span></span> <br/> |[<span data-ttu-id="4ed49-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="4ed49-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|<span data-ttu-id="4ed49-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="4ed49-118">RowDef</span></span> <br/> |[<span data-ttu-id="4ed49-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="4ed49-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4ed49-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="4ed49-120">Attributes</span></span>

|<span data-ttu-id="4ed49-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4ed49-121">**Attribute**</span></span>|<span data-ttu-id="4ed49-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4ed49-122">**Type**</span></span>|<span data-ttu-id="4ed49-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="4ed49-123">**Required**</span></span>|<span data-ttu-id="4ed49-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4ed49-124">**Description**</span></span>|<span data-ttu-id="4ed49-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="4ed49-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4ed49-126">N</span><span class="sxs-lookup"><span data-stu-id="4ed49-126">N</span></span>  <br/> |<span data-ttu-id="4ed49-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ed49-127">xsd:string</span></span>  <br/> |<span data-ttu-id="4ed49-128">obrigatório</span><span class="sxs-lookup"><span data-stu-id="4ed49-128">required</span></span>  <br/> ||<span data-ttu-id="4ed49-129">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ed49-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="4ed49-130">S</span><span class="sxs-lookup"><span data-stu-id="4ed49-130">S</span></span>  <br/> |<span data-ttu-id="4ed49-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="4ed49-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="4ed49-132">opcional</span><span class="sxs-lookup"><span data-stu-id="4ed49-132">optional</span></span>  <br/> ||<span data-ttu-id="4ed49-133">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="4ed49-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="4ed49-134">T</span><span class="sxs-lookup"><span data-stu-id="4ed49-134">T</span></span>  <br/> |<span data-ttu-id="4ed49-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="4ed49-135">xsd:string</span></span>  <br/> |<span data-ttu-id="4ed49-136">opcional</span><span class="sxs-lookup"><span data-stu-id="4ed49-136">optional</span></span>  <br/> ||<span data-ttu-id="4ed49-137">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="4ed49-137">Values of the xsd:string type.</span></span>  <br/> |
   

