---
title: Elemento Solution (Solutions_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Especifica uma instância da solução que XML armazenado no desenho.
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773032"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="347bc-103">Elemento Solution (Solutions_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="347bc-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="347bc-104">Especifica uma instância da solução que XML armazenado no desenho.</span><span class="sxs-lookup"><span data-stu-id="347bc-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="347bc-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="347bc-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="347bc-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="347bc-106">**Element type**</span></span> <br/> |[<span data-ttu-id="347bc-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="347bc-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="347bc-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="347bc-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="347bc-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="347bc-109">**Schema file**</span></span> <br/> |<span data-ttu-id="347bc-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="347bc-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="347bc-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="347bc-111">**Document parts**</span></span> <br/> |<span data-ttu-id="347bc-112">Solutions.XML</span><span class="sxs-lookup"><span data-stu-id="347bc-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="347bc-113">Definição</span><span class="sxs-lookup"><span data-stu-id="347bc-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="347bc-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="347bc-114">Elements and attributes</span></span>

<span data-ttu-id="347bc-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="347bc-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="347bc-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="347bc-116">Parent elements</span></span>

|<span data-ttu-id="347bc-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="347bc-117">**Element**</span></span>|<span data-ttu-id="347bc-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="347bc-118">**Type**</span></span>|<span data-ttu-id="347bc-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="347bc-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="347bc-120">Soluções</span><span class="sxs-lookup"><span data-stu-id="347bc-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="347bc-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="347bc-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="347bc-122">Armazena as propriedades das soluções armazenadas no documento.</span><span class="sxs-lookup"><span data-stu-id="347bc-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="347bc-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="347bc-123">Child elements</span></span>

|<span data-ttu-id="347bc-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="347bc-124">**Element**</span></span>|<span data-ttu-id="347bc-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="347bc-125">**Type**</span></span>|<span data-ttu-id="347bc-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="347bc-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="347bc-127">Rel</span><span class="sxs-lookup"><span data-stu-id="347bc-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="347bc-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="347bc-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="347bc-129">Especifica a relação a uma parte com a solução que XML associada a essa solução.</span><span class="sxs-lookup"><span data-stu-id="347bc-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="347bc-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="347bc-130">Attributes</span></span>

|<span data-ttu-id="347bc-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="347bc-131">**Attribute**</span></span>|<span data-ttu-id="347bc-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="347bc-132">**Type**</span></span>|<span data-ttu-id="347bc-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="347bc-133">**Required**</span></span>|<span data-ttu-id="347bc-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="347bc-134">**Description**</span></span>|<span data-ttu-id="347bc-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="347bc-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="347bc-136">Nome</span><span class="sxs-lookup"><span data-stu-id="347bc-136">Name</span></span>  <br/> |<span data-ttu-id="347bc-137">XSD: String</span><span class="sxs-lookup"><span data-stu-id="347bc-137">xsd:string</span></span>  <br/> |<span data-ttu-id="347bc-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="347bc-138">required</span></span>  <br/> |<span data-ttu-id="347bc-139">O nome da solução.</span><span class="sxs-lookup"><span data-stu-id="347bc-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="347bc-140">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="347bc-140">Values of the xsd:string type.</span></span>  <br/> |
   

