---
title: Row_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5e5c420e-f384-7b62-c862-35aea16e6d55
ms.openlocfilehash: dfa3a90aaec51ba89845934c1d4fad484914afa7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772795"
---
# <a name="rowtype-complextype-visio-xml"></a><span data-ttu-id="705a0-102">Row_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="705a0-102">Row_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="705a0-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="705a0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="705a0-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="705a0-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="705a0-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="705a0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="705a0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="705a0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="705a0-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="705a0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="705a0-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="705a0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="705a0-109">Definição</span><span class="sxs-lookup"><span data-stu-id="705a0-109">Definition</span></span>

```XML
          <xs:complexType name="Row_Type">
          
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="Trigger"  type="Trigger_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
    />
    <xs:attribute name="LocalName"
  type="xsd:string"
    />
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="T"
  type="xsd:string"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="705a0-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="705a0-110">Elements and attributes</span></span>

<span data-ttu-id="705a0-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="705a0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="705a0-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="705a0-112">Child elements</span></span>

|<span data-ttu-id="705a0-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="705a0-113">**Element**</span></span>|<span data-ttu-id="705a0-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="705a0-114">**Type**</span></span>|<span data-ttu-id="705a0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="705a0-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="705a0-116">Célula</span><span class="sxs-lookup"><span data-stu-id="705a0-116">Cell</span></span>](http://msdn.microsoft.com/library/5e060a3f-e804-834f-531b-78a544fee61f%28Office.15%29.aspx) <br/> |[<span data-ttu-id="705a0-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="705a0-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="705a0-118">Trigger</span><span class="sxs-lookup"><span data-stu-id="705a0-118">Trigger</span></span>](http://msdn.microsoft.com/library/6dbd2c66-3b29-03f6-648f-723d359ded0d%28Office.15%29.aspx) <br/> |[<span data-ttu-id="705a0-119">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="705a0-119">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="705a0-120">Atributos</span><span class="sxs-lookup"><span data-stu-id="705a0-120">Attributes</span></span>

|<span data-ttu-id="705a0-121">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="705a0-121">**Attribute**</span></span>|<span data-ttu-id="705a0-122">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="705a0-122">**Type**</span></span>|<span data-ttu-id="705a0-123">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="705a0-123">**Required**</span></span>|<span data-ttu-id="705a0-124">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="705a0-124">**Description**</span></span>|<span data-ttu-id="705a0-125">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="705a0-125">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="705a0-126">DEL</span><span class="sxs-lookup"><span data-stu-id="705a0-126">Del</span></span>  <br/> |<span data-ttu-id="705a0-127">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="705a0-127">xsd:boolean</span></span>  <br/> |<span data-ttu-id="705a0-128">opcional</span><span class="sxs-lookup"><span data-stu-id="705a0-128">optional</span></span>  <br/> ||<span data-ttu-id="705a0-129">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="705a0-129">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="705a0-130">IX</span><span class="sxs-lookup"><span data-stu-id="705a0-130">IX</span></span>  <br/> |<span data-ttu-id="705a0-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="705a0-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="705a0-132">opcional</span><span class="sxs-lookup"><span data-stu-id="705a0-132">optional</span></span>  <br/> ||<span data-ttu-id="705a0-133">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="705a0-133">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="705a0-134">LocalName</span><span class="sxs-lookup"><span data-stu-id="705a0-134">LocalName</span></span>  <br/> |<span data-ttu-id="705a0-135">XSD: String</span><span class="sxs-lookup"><span data-stu-id="705a0-135">xsd:string</span></span>  <br/> |<span data-ttu-id="705a0-136">opcional</span><span class="sxs-lookup"><span data-stu-id="705a0-136">optional</span></span>  <br/> ||<span data-ttu-id="705a0-137">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="705a0-137">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="705a0-138">N</span><span class="sxs-lookup"><span data-stu-id="705a0-138">N</span></span>  <br/> |<span data-ttu-id="705a0-139">XSD: String</span><span class="sxs-lookup"><span data-stu-id="705a0-139">xsd:string</span></span>  <br/> |<span data-ttu-id="705a0-140">opcional</span><span class="sxs-lookup"><span data-stu-id="705a0-140">optional</span></span>  <br/> ||<span data-ttu-id="705a0-141">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="705a0-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="705a0-142">T</span><span class="sxs-lookup"><span data-stu-id="705a0-142">T</span></span>  <br/> |<span data-ttu-id="705a0-143">XSD: String</span><span class="sxs-lookup"><span data-stu-id="705a0-143">xsd:string</span></span>  <br/> |<span data-ttu-id="705a0-144">opcional</span><span class="sxs-lookup"><span data-stu-id="705a0-144">optional</span></span>  <br/> ||<span data-ttu-id="705a0-145">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="705a0-145">Values of the xsd:string type.</span></span>  <br/> |
   

