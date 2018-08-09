---
title: DataRecordSets_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: b646e7a0d4e1f49aa71b162aecdd901813b01f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771668"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="62a2d-102">DataRecordSets_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="62a2d-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="62a2d-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="62a2d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62a2d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="62a2d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="62a2d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="62a2d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="62a2d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="62a2d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="62a2d-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="62a2d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="62a2d-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="62a2d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62a2d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="62a2d-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSets_Type">
          
          <xs:sequence>
    <xs:element name="DataRecordSet"  type="DataRecordSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ActiveRecordsetID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DataWindowOrder"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62a2d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="62a2d-110">Elements and attributes</span></span>

<span data-ttu-id="62a2d-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="62a2d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="62a2d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="62a2d-112">Child elements</span></span>

|<span data-ttu-id="62a2d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="62a2d-113">**Element**</span></span>|<span data-ttu-id="62a2d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="62a2d-114">**Type**</span></span>|<span data-ttu-id="62a2d-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62a2d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62a2d-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="62a2d-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62a2d-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="62a2d-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="62a2d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="62a2d-118">Attributes</span></span>

|<span data-ttu-id="62a2d-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="62a2d-119">**Attribute**</span></span>|<span data-ttu-id="62a2d-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="62a2d-120">**Type**</span></span>|<span data-ttu-id="62a2d-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="62a2d-121">**Required**</span></span>|<span data-ttu-id="62a2d-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="62a2d-122">**Description**</span></span>|<span data-ttu-id="62a2d-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="62a2d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62a2d-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="62a2d-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="62a2d-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="62a2d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="62a2d-126">opcional</span><span class="sxs-lookup"><span data-stu-id="62a2d-126">optional</span></span>  <br/> ||<span data-ttu-id="62a2d-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="62a2d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="62a2d-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="62a2d-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="62a2d-129">XSD: String</span><span class="sxs-lookup"><span data-stu-id="62a2d-129">xsd:string</span></span>  <br/> |<span data-ttu-id="62a2d-130">opcional</span><span class="sxs-lookup"><span data-stu-id="62a2d-130">optional</span></span>  <br/> ||<span data-ttu-id="62a2d-131">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="62a2d-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="62a2d-132">NextID</span><span class="sxs-lookup"><span data-stu-id="62a2d-132">NextID</span></span>  <br/> |<span data-ttu-id="62a2d-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="62a2d-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="62a2d-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="62a2d-134">required</span></span>  <br/> ||<span data-ttu-id="62a2d-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="62a2d-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

