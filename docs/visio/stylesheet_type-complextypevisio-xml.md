---
title: StyleSheet_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 06a02d07-920e-7d47-d63a-da3596cf20f6
ms.openlocfilehash: 394712b65ee44a939a20fd3b65df504785f106ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773090"
---
# <a name="stylesheettype-complextype-visio-xml"></a><span data-ttu-id="316c9-102">StyleSheet_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="316c9-102">StyleSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="316c9-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="316c9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="316c9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="316c9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="316c9-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="316c9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="316c9-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="316c9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="316c9-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="316c9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="316c9-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="316c9-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="316c9-109">Definição</span><span class="sxs-lookup"><span data-stu-id="316c9-109">Definition</span></span>

```XML
      <xs:complexType name="StyleSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
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
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="316c9-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="316c9-110">Elements and attributes</span></span>

<span data-ttu-id="316c9-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="316c9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="316c9-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="316c9-112">Child elements</span></span>

<span data-ttu-id="316c9-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="316c9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="316c9-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="316c9-114">Attributes</span></span>

|<span data-ttu-id="316c9-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="316c9-115">**Attribute**</span></span>|<span data-ttu-id="316c9-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="316c9-116">**Type**</span></span>|<span data-ttu-id="316c9-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="316c9-117">**Required**</span></span>|<span data-ttu-id="316c9-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="316c9-118">**Description**</span></span>|<span data-ttu-id="316c9-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="316c9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="316c9-120">ID</span><span class="sxs-lookup"><span data-stu-id="316c9-120">ID</span></span>  <br/> |<span data-ttu-id="316c9-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="316c9-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="316c9-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="316c9-122">required</span></span>  <br/> ||<span data-ttu-id="316c9-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="316c9-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="316c9-124">IsCustomName</span><span class="sxs-lookup"><span data-stu-id="316c9-124">IsCustomName</span></span>  <br/> |<span data-ttu-id="316c9-125">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="316c9-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="316c9-126">opcional</span><span class="sxs-lookup"><span data-stu-id="316c9-126">optional</span></span>  <br/> ||<span data-ttu-id="316c9-127">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="316c9-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="316c9-128">IsCustomNameU</span><span class="sxs-lookup"><span data-stu-id="316c9-128">IsCustomNameU</span></span>  <br/> |<span data-ttu-id="316c9-129">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="316c9-129">xsd:boolean</span></span>  <br/> |<span data-ttu-id="316c9-130">opcional</span><span class="sxs-lookup"><span data-stu-id="316c9-130">optional</span></span>  <br/> ||<span data-ttu-id="316c9-131">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="316c9-131">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="316c9-132">Nome</span><span class="sxs-lookup"><span data-stu-id="316c9-132">Name</span></span>  <br/> |<span data-ttu-id="316c9-133">XSD: String</span><span class="sxs-lookup"><span data-stu-id="316c9-133">xsd:string</span></span>  <br/> |<span data-ttu-id="316c9-134">opcional</span><span class="sxs-lookup"><span data-stu-id="316c9-134">optional</span></span>  <br/> ||<span data-ttu-id="316c9-135">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="316c9-135">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="316c9-136">NameU</span><span class="sxs-lookup"><span data-stu-id="316c9-136">NameU</span></span>  <br/> |<span data-ttu-id="316c9-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="316c9-137">xsd:string</span></span>  <br/> |<span data-ttu-id="316c9-138">opcional</span><span class="sxs-lookup"><span data-stu-id="316c9-138">optional</span></span>  <br/> ||<span data-ttu-id="316c9-139">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="316c9-139">Values of the xsd:string type.</span></span>  <br/> |
   

