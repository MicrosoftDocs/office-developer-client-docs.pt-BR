---
title: Issue_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d6768062-37aa-5658-f068-dae8d3a24717
ms.openlocfilehash: 1cdc38db93da57969230c280a2df24ac3b20ad0d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399694"
---
# <a name="issuetype-complextype-visio-xml"></a><span data-ttu-id="d8ecd-102">Issue_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d8ecd-102">Issue_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="d8ecd-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="d8ecd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d8ecd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="d8ecd-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="d8ecd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="d8ecd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="d8ecd-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="d8ecd-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d8ecd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d8ecd-109">Definição</span><span class="sxs-lookup"><span data-stu-id="d8ecd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d8ecd-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="d8ecd-110">Elements and attributes</span></span>

<span data-ttu-id="d8ecd-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="d8ecd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d8ecd-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="d8ecd-112">Child elements</span></span>

|<span data-ttu-id="d8ecd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-113">**Element**</span></span>|<span data-ttu-id="d8ecd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-114">**Type**</span></span>|<span data-ttu-id="d8ecd-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d8ecd-116">IssueTarget</span><span class="sxs-lookup"><span data-stu-id="d8ecd-116">IssueTarget</span></span>](issuetarget-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8ecd-117">IssueTarget_Type</span><span class="sxs-lookup"><span data-stu-id="d8ecd-117">IssueTarget_Type</span></span>](issuetarget_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="d8ecd-118">RuleInfo</span><span class="sxs-lookup"><span data-stu-id="d8ecd-118">RuleInfo</span></span>](ruleinfo-element-issue_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d8ecd-119">RuleInfo_Type</span><span class="sxs-lookup"><span data-stu-id="d8ecd-119">RuleInfo_Type</span></span>](ruleinfo_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="d8ecd-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="d8ecd-120">Attributes</span></span>

|<span data-ttu-id="d8ecd-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-121">**Attribute**</span></span>|<span data-ttu-id="d8ecd-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-122">**Type**</span></span>|<span data-ttu-id="d8ecd-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-123">**Required**</span></span>|<span data-ttu-id="d8ecd-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-124">**Description**</span></span>|<span data-ttu-id="d8ecd-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="d8ecd-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8ecd-126">ID</span><span class="sxs-lookup"><span data-stu-id="d8ecd-126">ID</span></span>  <br/> |<span data-ttu-id="d8ecd-127">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d8ecd-127">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d8ecd-128">obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8ecd-128">required</span></span>  <br/> ||<span data-ttu-id="d8ecd-129">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d8ecd-129">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d8ecd-130">Ignorado</span><span class="sxs-lookup"><span data-stu-id="d8ecd-130">Ignored</span></span>  <br/> |<span data-ttu-id="d8ecd-131">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="d8ecd-131">xsd:boolean</span></span>  <br/> |<span data-ttu-id="d8ecd-132">opcional</span><span class="sxs-lookup"><span data-stu-id="d8ecd-132">optional</span></span>  <br/> ||<span data-ttu-id="d8ecd-133">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="d8ecd-133">Values of the xsd:boolean type.</span></span>  <br/> |
   

