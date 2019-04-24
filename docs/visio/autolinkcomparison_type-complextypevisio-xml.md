---
title: AutoLinkComparison_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 319b4bfb-a798-4f6c-52be-45708ac40869
ms.openlocfilehash: 235b63777d21955a2f2062757d6a54e899b169ac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338595"
---
# <a name="autolinkcomparisontype-complextype-visio-xml"></a><span data-ttu-id="536ac-102">AutoLinkComparison_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="536ac-102">AutoLinkComparison_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="536ac-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="536ac-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="536ac-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="536ac-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="536ac-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="536ac-105">**Schema file**</span></span> <br/> |<span data-ttu-id="536ac-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="536ac-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="536ac-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="536ac-107">**Extension base**</span></span> <br/> |<span data-ttu-id="536ac-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="536ac-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="536ac-109">Definição</span><span class="sxs-lookup"><span data-stu-id="536ac-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="536ac-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="536ac-110">Elements and attributes</span></span>

<span data-ttu-id="536ac-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="536ac-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="536ac-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="536ac-112">Child elements</span></span>

<span data-ttu-id="536ac-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="536ac-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="536ac-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="536ac-114">Attributes</span></span>

|<span data-ttu-id="536ac-115">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="536ac-115">**Attribute**</span></span>|<span data-ttu-id="536ac-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="536ac-116">**Type**</span></span>|<span data-ttu-id="536ac-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="536ac-117">**Required**</span></span>|<span data-ttu-id="536ac-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="536ac-118">**Description**</span></span>|<span data-ttu-id="536ac-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="536ac-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="536ac-120">ColumnName</span><span class="sxs-lookup"><span data-stu-id="536ac-120">ColumnName</span></span>  <br/> |<span data-ttu-id="536ac-121">xsd:string</span><span class="sxs-lookup"><span data-stu-id="536ac-121">xsd:string</span></span>  <br/> |<span data-ttu-id="536ac-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="536ac-122">required</span></span>  <br/> ||<span data-ttu-id="536ac-123">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="536ac-123">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="536ac-124">ContextType</span><span class="sxs-lookup"><span data-stu-id="536ac-124">ContextType</span></span>  <br/> |<span data-ttu-id="536ac-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="536ac-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="536ac-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="536ac-126">required</span></span>  <br/> ||<span data-ttu-id="536ac-127">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="536ac-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="536ac-128">ContextTypeLabel</span><span class="sxs-lookup"><span data-stu-id="536ac-128">ContextTypeLabel</span></span>  <br/> |<span data-ttu-id="536ac-129">xsd:string</span><span class="sxs-lookup"><span data-stu-id="536ac-129">xsd:string</span></span>  <br/> |<span data-ttu-id="536ac-130">opcional</span><span class="sxs-lookup"><span data-stu-id="536ac-130">optional</span></span>  <br/> ||<span data-ttu-id="536ac-131">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="536ac-131">Values of the xsd:string type.</span></span>  <br/> |
   

