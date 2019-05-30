---
title: DataRecordSets_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 77a6588a1b5fba05d14e91a39ba570d21142f953
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539155"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="9a5fa-102">DataRecordSets_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="9a5fa-102">DataRecordSets_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="9a5fa-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="9a5fa-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9a5fa-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9a5fa-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9a5fa-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9a5fa-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9a5fa-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9a5fa-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9a5fa-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9a5fa-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9a5fa-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9a5fa-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9a5fa-110">Elements and attributes</span></span>

<span data-ttu-id="9a5fa-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9a5fa-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9a5fa-112">Child elements</span></span>

|<span data-ttu-id="9a5fa-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-113">**Element**</span></span>|<span data-ttu-id="9a5fa-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-114">**Type**</span></span>|<span data-ttu-id="9a5fa-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9a5fa-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="9a5fa-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9a5fa-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="9a5fa-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9a5fa-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9a5fa-118">Attributes</span></span>

|<span data-ttu-id="9a5fa-119">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-119">**Attribute**</span></span>|<span data-ttu-id="9a5fa-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-120">**Type**</span></span>|<span data-ttu-id="9a5fa-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-121">**Required**</span></span>|<span data-ttu-id="9a5fa-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-122">**Description**</span></span>|<span data-ttu-id="9a5fa-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9a5fa-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9a5fa-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="9a5fa-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="9a5fa-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a5fa-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a5fa-126">opcional</span><span class="sxs-lookup"><span data-stu-id="9a5fa-126">optional</span></span>  <br/> ||<span data-ttu-id="9a5fa-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9a5fa-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="9a5fa-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="9a5fa-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="9a5fa-129">xsd:string</span></span>  <br/> |<span data-ttu-id="9a5fa-130">opcional</span><span class="sxs-lookup"><span data-stu-id="9a5fa-130">optional</span></span>  <br/> ||<span data-ttu-id="9a5fa-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="9a5fa-132">NextID</span><span class="sxs-lookup"><span data-stu-id="9a5fa-132">NextID</span></span>  <br/> |<span data-ttu-id="9a5fa-133">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9a5fa-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9a5fa-134">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9a5fa-134">required</span></span>  <br/> ||<span data-ttu-id="9a5fa-135">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9a5fa-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

