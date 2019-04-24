---
title: DataRecordSets_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360344"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="441c6-102">DataRecordSets_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="441c6-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="441c6-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="441c6-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="441c6-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="441c6-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="441c6-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="441c6-105">**Schema file**</span></span> <br/> |<span data-ttu-id="441c6-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="441c6-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="441c6-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="441c6-107">**Extension base**</span></span> <br/> |<span data-ttu-id="441c6-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="441c6-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="441c6-109">Definição</span><span class="sxs-lookup"><span data-stu-id="441c6-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="441c6-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="441c6-110">Elements and attributes</span></span>

<span data-ttu-id="441c6-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="441c6-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="441c6-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="441c6-112">Child elements</span></span>

|<span data-ttu-id="441c6-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="441c6-113">**Element**</span></span>|<span data-ttu-id="441c6-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="441c6-114">**Type**</span></span>|<span data-ttu-id="441c6-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="441c6-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="441c6-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="441c6-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="441c6-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="441c6-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="441c6-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="441c6-118">Attributes</span></span>

|<span data-ttu-id="441c6-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="441c6-119">**Attribute**</span></span>|<span data-ttu-id="441c6-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="441c6-120">**Type**</span></span>|<span data-ttu-id="441c6-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="441c6-121">**Required**</span></span>|<span data-ttu-id="441c6-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="441c6-122">**Description**</span></span>|<span data-ttu-id="441c6-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="441c6-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="441c6-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="441c6-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="441c6-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="441c6-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="441c6-126">opcional</span><span class="sxs-lookup"><span data-stu-id="441c6-126">optional</span></span>  <br/> ||<span data-ttu-id="441c6-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="441c6-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="441c6-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="441c6-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="441c6-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="441c6-129">xsd:string</span></span>  <br/> |<span data-ttu-id="441c6-130">opcional</span><span class="sxs-lookup"><span data-stu-id="441c6-130">optional</span></span>  <br/> ||<span data-ttu-id="441c6-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="441c6-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="441c6-132">NextID</span><span class="sxs-lookup"><span data-stu-id="441c6-132">NextID</span></span>  <br/> |<span data-ttu-id="441c6-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="441c6-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="441c6-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="441c6-134">required</span></span>  <br/> ||<span data-ttu-id="441c6-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="441c6-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

