---
title: SectionDef_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ab57bf2-0d9f-4a3a-4882-c77d7c781cbd
ms.openlocfilehash: 426e62ea7a9f990555776e3ac732dd43e614582d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772854"
---
# <a name="sectiondeftype-complextype-visio-xml"></a><span data-ttu-id="ce64b-102">SectionDef_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ce64b-102">SectionDef_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ce64b-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="ce64b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ce64b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ce64b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ce64b-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="ce64b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ce64b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ce64b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ce64b-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="ce64b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ce64b-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ce64b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ce64b-109">Definição</span><span class="sxs-lookup"><span data-stu-id="ce64b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ce64b-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="ce64b-110">Elements and attributes</span></span>

<span data-ttu-id="ce64b-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="ce64b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ce64b-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="ce64b-112">Child elements</span></span>

|<span data-ttu-id="ce64b-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ce64b-113">**Element**</span></span>|<span data-ttu-id="ce64b-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ce64b-114">**Type**</span></span>|<span data-ttu-id="ce64b-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ce64b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ce64b-116">CellDef</span><span class="sxs-lookup"><span data-stu-id="ce64b-116">CellDef</span></span>](http://msdn.microsoft.com/library/f0ec7afe-9e0a-b5e5-82dd-4adff1c1607f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ce64b-117">CellDef_Type</span><span class="sxs-lookup"><span data-stu-id="ce64b-117">CellDef_Type</span></span>](celldef_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="ce64b-118">RowDef</span><span class="sxs-lookup"><span data-stu-id="ce64b-118">RowDef</span></span>](http://msdn.microsoft.com/library/25615be9-1d19-1ba9-4192-7d4a0dfae717%28Office.15%29.aspx) <br/> |[<span data-ttu-id="ce64b-119">RowDef_Type</span><span class="sxs-lookup"><span data-stu-id="ce64b-119">RowDef_Type</span></span>](rowdef_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ce64b-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="ce64b-120">Attributes</span></span>

|<span data-ttu-id="ce64b-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ce64b-121">**Attribute**</span></span>|<span data-ttu-id="ce64b-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="ce64b-122">**Type**</span></span>|<span data-ttu-id="ce64b-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="ce64b-123">**Required**</span></span>|<span data-ttu-id="ce64b-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ce64b-124">**Description**</span></span>|<span data-ttu-id="ce64b-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="ce64b-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ce64b-126">N</span><span class="sxs-lookup"><span data-stu-id="ce64b-126">N</span></span>  <br/> |<span data-ttu-id="ce64b-127">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ce64b-127">xsd:string</span></span>  <br/> |<span data-ttu-id="ce64b-128">obrigatório</span><span class="sxs-lookup"><span data-stu-id="ce64b-128">required</span></span>  <br/> ||<span data-ttu-id="ce64b-129">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ce64b-129">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ce64b-130">S</span><span class="sxs-lookup"><span data-stu-id="ce64b-130">S</span></span>  <br/> |<span data-ttu-id="ce64b-131">XSD:unsignedByte</span><span class="sxs-lookup"><span data-stu-id="ce64b-131">xsd:unsignedByte</span></span>  <br/> |<span data-ttu-id="ce64b-132">opcional</span><span class="sxs-lookup"><span data-stu-id="ce64b-132">optional</span></span>  <br/> ||<span data-ttu-id="ce64b-133">Valores do tipo xsd:unsignedByte.</span><span class="sxs-lookup"><span data-stu-id="ce64b-133">Values of the xsd:unsignedByte type.</span></span>  <br/> |
|<span data-ttu-id="ce64b-134">T</span><span class="sxs-lookup"><span data-stu-id="ce64b-134">T</span></span>  <br/> |<span data-ttu-id="ce64b-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="ce64b-135">xsd:string</span></span>  <br/> |<span data-ttu-id="ce64b-136">opcional</span><span class="sxs-lookup"><span data-stu-id="ce64b-136">optional</span></span>  <br/> ||<span data-ttu-id="ce64b-137">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="ce64b-137">Values of the xsd:string type.</span></span>  <br/> |
   

