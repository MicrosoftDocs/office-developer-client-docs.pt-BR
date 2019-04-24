---
title: Issue_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339498"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="cc47e-102">Issue_Type complexType (' Visio XML ')</span><span class="sxs-lookup"><span data-stu-id="cc47e-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="cc47e-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="cc47e-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cc47e-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cc47e-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="cc47e-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="cc47e-105">**Schema file**</span></span> <br/> |<span data-ttu-id="cc47e-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="cc47e-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="cc47e-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="cc47e-107">**Extension base**</span></span> <br/> |<span data-ttu-id="cc47e-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="cc47e-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cc47e-109">Definição</span><span class="sxs-lookup"><span data-stu-id="cc47e-109">Definition</span></span>

```XML
          <xs:complexType name="Issue_Type">
          
          <xs:sequence>
    <xs:element name="IssueTarget"  type="IssueTarget_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="RuleInfo"  type="RuleInfo_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Ignored"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cc47e-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="cc47e-110">Elements and attributes</span></span>

<span data-ttu-id="cc47e-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="cc47e-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="cc47e-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="cc47e-112">Child elements</span></span>

|<span data-ttu-id="cc47e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cc47e-113">**Element**</span></span>|<span data-ttu-id="cc47e-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc47e-114">**Type**</span></span>|<span data-ttu-id="cc47e-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc47e-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cc47e-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="cc47e-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc47e-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="cc47e-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="cc47e-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="cc47e-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cc47e-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="cc47e-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="cc47e-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="cc47e-120">Attributes</span></span>

|<span data-ttu-id="cc47e-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="cc47e-121">**Attribute**</span></span>|<span data-ttu-id="cc47e-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="cc47e-122">**Type**</span></span>|<span data-ttu-id="cc47e-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="cc47e-123">**Required**</span></span>|<span data-ttu-id="cc47e-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cc47e-124">**Description**</span></span>|<span data-ttu-id="cc47e-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="cc47e-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cc47e-126">ID</span><span class="sxs-lookup"><span data-stu-id="cc47e-126">ID</span></span>  <br/> |<span data-ttu-id="cc47e-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cc47e-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cc47e-128">obrigatório</span><span class="sxs-lookup"><span data-stu-id="cc47e-128">required</span></span>  <br/> ||<span data-ttu-id="cc47e-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cc47e-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cc47e-130">Ignorado</span><span class="sxs-lookup"><span data-stu-id="cc47e-130">Ignored</span></span>  <br/> |<span data-ttu-id="cc47e-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="cc47e-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="cc47e-132">opcional</span><span class="sxs-lookup"><span data-stu-id="cc47e-132">optional</span></span>  <br/> ||<span data-ttu-id="cc47e-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="cc47e-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

