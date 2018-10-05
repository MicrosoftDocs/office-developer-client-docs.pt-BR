---
title: HeaderFooter_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5fcf3d9-c11a-ed5e-0bf5-e706259ef30b
ms.openlocfilehash: 581101909096d4ee8a4f44c8e9e95dab0313ed7c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384504"
---
# <a name="headerfootertype-complextype-visio-xml"></a><span data-ttu-id="48972-102">HeaderFooter_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="48972-102">HeaderFooter_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="48972-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="48972-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48972-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="48972-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="48972-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="48972-105">**Schema file**</span></span> <br/> |<span data-ttu-id="48972-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="48972-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="48972-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="48972-107">**Extension base**</span></span> <br/> |<span data-ttu-id="48972-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="48972-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48972-109">Definição</span><span class="sxs-lookup"><span data-stu-id="48972-109">Definition</span></span>

```XML
          <xs:complexType name="HeaderFooter_Type">
          
          <xs:all>
    <xs:element name="HeaderMargin"  type="HeaderMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterMargin"  type="FooterMargin_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderLeft"  type="HeaderLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderCenter"  type="HeaderCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderRight"  type="HeaderRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterLeft"  type="FooterLeft_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterCenter"  type="FooterCenter_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="FooterRight"  type="FooterRight_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="HeaderFooterFont"  type="HeaderFooterFont_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="HeaderFooterColor"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="48972-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="48972-110">Elements and attributes</span></span>

<span data-ttu-id="48972-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="48972-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48972-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="48972-112">Child elements</span></span>

|<span data-ttu-id="48972-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="48972-113">**Element**</span></span>|<span data-ttu-id="48972-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48972-114">**Type**</span></span>|<span data-ttu-id="48972-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48972-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48972-116">FooterCenter</span><span class="sxs-lookup"><span data-stu-id="48972-116">FooterCenter</span></span>](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-117">FooterCenter_Type</span><span class="sxs-lookup"><span data-stu-id="48972-117">FooterCenter_Type</span></span>](footercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-118">FooterLeft</span><span class="sxs-lookup"><span data-stu-id="48972-118">FooterLeft</span></span>](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-119">FooterLeft_Type</span><span class="sxs-lookup"><span data-stu-id="48972-119">FooterLeft_Type</span></span>](footerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-120">FooterMargin</span><span class="sxs-lookup"><span data-stu-id="48972-120">FooterMargin</span></span>](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-121">FooterMargin_Type</span><span class="sxs-lookup"><span data-stu-id="48972-121">FooterMargin_Type</span></span>](footermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-122">FooterRight</span><span class="sxs-lookup"><span data-stu-id="48972-122">FooterRight</span></span>](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-123">FooterRight_Type</span><span class="sxs-lookup"><span data-stu-id="48972-123">FooterRight_Type</span></span>](footerright_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-124">HeaderCenter</span><span class="sxs-lookup"><span data-stu-id="48972-124">HeaderCenter</span></span>](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-125">HeaderCenter_Type</span><span class="sxs-lookup"><span data-stu-id="48972-125">HeaderCenter_Type</span></span>](headercenter_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-126">HeaderFooterFont</span><span class="sxs-lookup"><span data-stu-id="48972-126">HeaderFooterFont</span></span>](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-127">HeaderFooterFont_Type</span><span class="sxs-lookup"><span data-stu-id="48972-127">HeaderFooterFont_Type</span></span>](headerfooterfont_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-128">HeaderLeft</span><span class="sxs-lookup"><span data-stu-id="48972-128">HeaderLeft</span></span>](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-129">HeaderLeft_Type</span><span class="sxs-lookup"><span data-stu-id="48972-129">HeaderLeft_Type</span></span>](headerleft_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-130">HeaderMargin</span><span class="sxs-lookup"><span data-stu-id="48972-130">HeaderMargin</span></span>](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-131">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="48972-131">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="48972-132">HeaderRight</span><span class="sxs-lookup"><span data-stu-id="48972-132">HeaderRight</span></span>](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48972-133">HeaderRight_Type</span><span class="sxs-lookup"><span data-stu-id="48972-133">HeaderRight_Type</span></span>](headerright_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="48972-134">Atributos</span><span class="sxs-lookup"><span data-stu-id="48972-134">Attributes</span></span>

|<span data-ttu-id="48972-135">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="48972-135">**Attribute**</span></span>|<span data-ttu-id="48972-136">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48972-136">**Type**</span></span>|<span data-ttu-id="48972-137">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="48972-137">**Required**</span></span>|<span data-ttu-id="48972-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48972-138">**Description**</span></span>|<span data-ttu-id="48972-139">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="48972-139">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48972-140">HeaderFooterColor</span><span class="sxs-lookup"><span data-stu-id="48972-140">HeaderFooterColor</span></span>  <br/> |<span data-ttu-id="48972-141">XSD: String</span><span class="sxs-lookup"><span data-stu-id="48972-141">xsd:string</span></span>  <br/> |<span data-ttu-id="48972-142">opcional</span><span class="sxs-lookup"><span data-stu-id="48972-142">optional</span></span>  <br/> ||<span data-ttu-id="48972-143">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="48972-143">Values of the xsd:string type.</span></span>  <br/> |
   

