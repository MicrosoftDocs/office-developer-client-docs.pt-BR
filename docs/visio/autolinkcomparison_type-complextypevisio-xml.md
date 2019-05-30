---
title: AutoLinkComparison_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: eeb58a0e2f401c0e8a2bcf67147bc300bb8535ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537882"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="57641-102">AutoLinkComparison_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="57641-102">AutoLinkComparison_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="57641-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="57641-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="57641-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="57641-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="57641-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="57641-105">**Schema file**</span></span> <br/> |<span data-ttu-id="57641-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="57641-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="57641-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="57641-107">**Extension base**</span></span> <br/> |<span data-ttu-id="57641-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="57641-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="57641-109">Definição</span><span class="sxs-lookup"><span data-stu-id="57641-109">Definition</span></span>

```XML
      <xs:complexType name="AutoLinkComparison_Type">
    <xs:attribute name="ColumnName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ContextType"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ContextTypeLabel"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="57641-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="57641-110">Elements and attributes</span></span>

<span data-ttu-id="57641-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="57641-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="57641-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="57641-112">Child elements</span></span>

<span data-ttu-id="57641-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="57641-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="57641-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="57641-114">Attributes</span></span>

|<span data-ttu-id="57641-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="57641-115">**Attribute**</span></span>|<span data-ttu-id="57641-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="57641-116">**Type**</span></span>|<span data-ttu-id="57641-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="57641-117">**Required**</span></span>|<span data-ttu-id="57641-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="57641-118">**Description**</span></span>|<span data-ttu-id="57641-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="57641-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="57641-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="57641-120">ColumnName</span></span>  <br/> |<span data-ttu-id="57641-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="57641-121">xsd:string</span></span>  <br/> |<span data-ttu-id="57641-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="57641-122">required</span></span>  <br/> ||<span data-ttu-id="57641-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="57641-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="57641-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="57641-124">ContextType</span></span>  <br/> |<span data-ttu-id="57641-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="57641-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="57641-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="57641-126">required</span></span>  <br/> ||<span data-ttu-id="57641-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="57641-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="57641-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="57641-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="57641-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="57641-129">xsd:string</span></span>  <br/> |<span data-ttu-id="57641-130">opcional</span><span class="sxs-lookup"><span data-stu-id="57641-130">optional</span></span>  <br/> ||<span data-ttu-id="57641-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="57641-131">Values of the xsd:string type.</span></span>  <br/> |
   

