---
title: Issue_Type complexType (XML do Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: b351554fe7919cada99172f721f5dbe2fd8f243a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542958"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="c25b8-102">Issue_Type complexType (XML do Visio)</span><span class="sxs-lookup"><span data-stu-id="c25b8-102">Issue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c25b8-103">Informação de tipo</span><span class="sxs-lookup"><span data-stu-id="c25b8-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c25b8-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c25b8-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c25b8-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="c25b8-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c25b8-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c25b8-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c25b8-107">**Base da extensão**</span><span class="sxs-lookup"><span data-stu-id="c25b8-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c25b8-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c25b8-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c25b8-109">Definição</span><span class="sxs-lookup"><span data-stu-id="c25b8-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c25b8-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="c25b8-110">Elements and attributes</span></span>

<span data-ttu-id="c25b8-111">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="c25b8-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c25b8-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="c25b8-112">Child elements</span></span>

|<span data-ttu-id="c25b8-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c25b8-113">**Element**</span></span>|<span data-ttu-id="c25b8-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c25b8-114">**Type**</span></span>|<span data-ttu-id="c25b8-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c25b8-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c25b8-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="c25b8-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c25b8-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="c25b8-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c25b8-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="c25b8-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c25b8-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="c25b8-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c25b8-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="c25b8-120">Attributes</span></span>

|<span data-ttu-id="c25b8-121">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="c25b8-121">**Attribute**</span></span>|<span data-ttu-id="c25b8-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="c25b8-122">**Type**</span></span>|<span data-ttu-id="c25b8-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="c25b8-123">**Required**</span></span>|<span data-ttu-id="c25b8-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c25b8-124">**Description**</span></span>|<span data-ttu-id="c25b8-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="c25b8-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c25b8-126">ID</span><span class="sxs-lookup"><span data-stu-id="c25b8-126">ID</span></span>  <br/> |<span data-ttu-id="c25b8-127">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c25b8-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c25b8-128">obrigatório</span><span class="sxs-lookup"><span data-stu-id="c25b8-128">required</span></span>  <br/> ||<span data-ttu-id="c25b8-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c25b8-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c25b8-130">Ignorado</span><span class="sxs-lookup"><span data-stu-id="c25b8-130">Ignored</span></span>  <br/> |<span data-ttu-id="c25b8-131">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="c25b8-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c25b8-132">opcional</span><span class="sxs-lookup"><span data-stu-id="c25b8-132">optional</span></span>  <br/> ||<span data-ttu-id="c25b8-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="c25b8-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

