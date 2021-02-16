---
title: DocumentSheet_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 57af2ed5-7d89-9538-e51b-0bc70f067b40
ms.openlocfilehash: 18e7f064b1b6c9ac8e084c96011c1b18a646aecb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540004"
---
# <a name="documentsheet_type-complextype-visio-xml"></a><span data-ttu-id="0c6ca-102">DocumentSheet_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="0c6ca-102">DocumentSheet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="0c6ca-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="0c6ca-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c6ca-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c6ca-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c6ca-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c6ca-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c6ca-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c6ca-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="0c6ca-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c6ca-109">Definição</span><span class="sxs-lookup"><span data-stu-id="0c6ca-109">Definition</span></span>

```XML
      <xs:complexType name="DocumentSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="0c6ca-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="0c6ca-110">Elements and attributes</span></span>

<span data-ttu-id="0c6ca-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c6ca-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="0c6ca-112">Child elements</span></span>

<span data-ttu-id="0c6ca-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c6ca-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0c6ca-114">Attributes</span></span>

|<span data-ttu-id="0c6ca-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-115">**Attribute**</span></span>|<span data-ttu-id="0c6ca-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-116">**Type**</span></span>|<span data-ttu-id="0c6ca-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-117">**Required**</span></span>|<span data-ttu-id="0c6ca-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-118">**Description**</span></span>|<span data-ttu-id="0c6ca-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="0c6ca-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c6ca-120">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="0c6ca-120">IsCustomName</span></span>  <br/> |<span data-ttu-id="0c6ca-121">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0c6ca-121">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c6ca-122">opcional</span><span class="sxs-lookup"><span data-stu-id="0c6ca-122">optional</span></span>  <br/> ||<span data-ttu-id="0c6ca-123">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-123">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c6ca-124">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="0c6ca-124">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="0c6ca-125">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="0c6ca-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="0c6ca-126">opcional</span><span class="sxs-lookup"><span data-stu-id="0c6ca-126">optional</span></span>  <br/> ||<span data-ttu-id="0c6ca-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="0c6ca-128">Nome</span><span class="sxs-lookup"><span data-stu-id="0c6ca-128">Name</span></span>  <br/> |<span data-ttu-id="0c6ca-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0c6ca-129">xsd:string</span></span>  <br/> |<span data-ttu-id="0c6ca-130">opcional</span><span class="sxs-lookup"><span data-stu-id="0c6ca-130">optional</span></span>  <br/> ||<span data-ttu-id="0c6ca-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c6ca-132">NameU</span><span class="sxs-lookup"><span data-stu-id="0c6ca-132">NameU</span></span>  <br/> |<span data-ttu-id="0c6ca-133">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0c6ca-133">xsd:string</span></span>  <br/> |<span data-ttu-id="0c6ca-134">opcional</span><span class="sxs-lookup"><span data-stu-id="0c6ca-134">optional</span></span>  <br/> ||<span data-ttu-id="0c6ca-135">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="0c6ca-136">UniqueID</span><span class="sxs-lookup"><span data-stu-id="0c6ca-136">UniqueID</span></span>  <br/> |<span data-ttu-id="0c6ca-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="0c6ca-137">xsd:string</span></span>  <br/> |<span data-ttu-id="0c6ca-138">opcional</span><span class="sxs-lookup"><span data-stu-id="0c6ca-138">optional</span></span>  <br/> ||<span data-ttu-id="0c6ca-139">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="0c6ca-139">Values of the xsd:string type.</span></span>  <br/> |
   

