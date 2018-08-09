---
title: Section_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f8e855f-064c-d286-560f-9f89e7fce7b7
ms.openlocfilehash: 8eb9362f84849ad22a20662b327ae33cd795cc5a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772848"
---
# <a name="sectiontype-complextype-visio-xml"></a><span data-ttu-id="215eb-102">Section_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="215eb-102">Section_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="215eb-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="215eb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="215eb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="215eb-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="215eb-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="215eb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="215eb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="215eb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="215eb-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="215eb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="215eb-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="215eb-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="215eb-109">Definição</span><span class="sxs-lookup"><span data-stu-id="215eb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="215eb-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="215eb-110">Elements and attributes</span></span>

<span data-ttu-id="215eb-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="215eb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="215eb-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="215eb-112">Child elements</span></span>

|<span data-ttu-id="215eb-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="215eb-113">**Element**</span></span>|<span data-ttu-id="215eb-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="215eb-114">**Type**</span></span>|<span data-ttu-id="215eb-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="215eb-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="215eb-116">Célula</span><span class="sxs-lookup"><span data-stu-id="215eb-116">Cell</span></span>](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[<span data-ttu-id="215eb-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="215eb-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="215eb-118">Row</span><span class="sxs-lookup"><span data-stu-id="215eb-118">Row</span></span>](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[<span data-ttu-id="215eb-119">Row_Type</span><span class="sxs-lookup"><span data-stu-id="215eb-119">Row_Type</span></span>](row_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="215eb-120">Trigger</span><span class="sxs-lookup"><span data-stu-id="215eb-120">Trigger</span></span>](http://msdn.microsoft.com/library/e4eeb238-f6d0-fb23-db1c-01d55b0a8d88%28Office.15%29.aspx) <br/> |[<span data-ttu-id="215eb-121">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="215eb-121">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="215eb-122">Atributos</span><span class="sxs-lookup"><span data-stu-id="215eb-122">Attributes</span></span>

|<span data-ttu-id="215eb-123">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="215eb-123">**Attribute**</span></span>|<span data-ttu-id="215eb-124">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="215eb-124">**Type**</span></span>|<span data-ttu-id="215eb-125">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="215eb-125">**Required**</span></span>|<span data-ttu-id="215eb-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="215eb-126">**Description**</span></span>|<span data-ttu-id="215eb-127">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="215eb-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="215eb-128">DEL</span><span class="sxs-lookup"><span data-stu-id="215eb-128">Del</span></span>  <br/> |<span data-ttu-id="215eb-129">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="215eb-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="215eb-130">opcional</span><span class="sxs-lookup"><span data-stu-id="215eb-130">optional</span></span>  <br/> ||<span data-ttu-id="215eb-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="215eb-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="215eb-132">IX</span><span class="sxs-lookup"><span data-stu-id="215eb-132">IX</span></span>  <br/> |<span data-ttu-id="215eb-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="215eb-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="215eb-134">opcional</span><span class="sxs-lookup"><span data-stu-id="215eb-134">optional</span></span>  <br/> ||<span data-ttu-id="215eb-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="215eb-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="215eb-136">N</span><span class="sxs-lookup"><span data-stu-id="215eb-136">N</span></span>  <br/> |<span data-ttu-id="215eb-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="215eb-137">xsd:string</span></span>  <br/> |<span data-ttu-id="215eb-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="215eb-138">required</span></span>  <br/> ||<span data-ttu-id="215eb-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="215eb-139">Values of the xsd:string type.</span></span>  <br/> |
   

