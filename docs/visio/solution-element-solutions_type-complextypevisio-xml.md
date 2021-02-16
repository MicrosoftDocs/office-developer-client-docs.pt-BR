---
title: Elemento Solution (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Especifica uma instância da solução XML armazenada no desenho.
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540263"
---
# <a name="solution-element-solutions_type-complextype-visio-xml"></a><span data-ttu-id="dc302-103">Elemento Solution (Solutions_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dc302-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="dc302-104">Especifica uma instância de SOLUÇÃO XML armazenada no desenho.</span><span class="sxs-lookup"><span data-stu-id="dc302-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dc302-105">Informações de elemento</span><span class="sxs-lookup"><span data-stu-id="dc302-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dc302-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="dc302-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dc302-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="dc302-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dc302-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dc302-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dc302-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="dc302-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dc302-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dc302-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dc302-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="dc302-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dc302-112">solutions.xml</span><span class="sxs-lookup"><span data-stu-id="dc302-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dc302-113">Definição</span><span class="sxs-lookup"><span data-stu-id="dc302-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dc302-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="dc302-114">Elements and attributes</span></span>

<span data-ttu-id="dc302-115">Se o esquema definir requisitos específicos, como **sequence**, **minOccurs**,**maxOccurs** e **choice**, confira a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="dc302-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dc302-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="dc302-116">Parent elements</span></span>

|<span data-ttu-id="dc302-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dc302-117">**Element**</span></span>|<span data-ttu-id="dc302-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dc302-118">**Type**</span></span>|<span data-ttu-id="dc302-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dc302-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dc302-120">Soluções</span><span class="sxs-lookup"><span data-stu-id="dc302-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="dc302-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="dc302-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dc302-122">Armazena as propriedades das soluções armazenadas no documento.</span><span class="sxs-lookup"><span data-stu-id="dc302-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dc302-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="dc302-123">Child elements</span></span>

|<span data-ttu-id="dc302-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="dc302-124">**Element**</span></span>|<span data-ttu-id="dc302-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dc302-125">**Type**</span></span>|<span data-ttu-id="dc302-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dc302-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dc302-127">Rel</span><span class="sxs-lookup"><span data-stu-id="dc302-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dc302-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="dc302-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dc302-129">Especifica a relação com uma parte com o XML da solução associado a essa solução.</span><span class="sxs-lookup"><span data-stu-id="dc302-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="dc302-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="dc302-130">Attributes</span></span>

|<span data-ttu-id="dc302-131">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="dc302-131">**Attribute**</span></span>|<span data-ttu-id="dc302-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="dc302-132">**Type**</span></span>|<span data-ttu-id="dc302-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="dc302-133">**Required**</span></span>|<span data-ttu-id="dc302-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dc302-134">**Description**</span></span>|<span data-ttu-id="dc302-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="dc302-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dc302-136">Nome</span><span class="sxs-lookup"><span data-stu-id="dc302-136">Name</span></span>  <br/> |<span data-ttu-id="dc302-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="dc302-137">xsd:string</span></span>  <br/> |<span data-ttu-id="dc302-138">obrigatório</span><span class="sxs-lookup"><span data-stu-id="dc302-138">required</span></span>  <br/> |<span data-ttu-id="dc302-139">O nome da solução.</span><span class="sxs-lookup"><span data-stu-id="dc302-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="dc302-140">Valores do tipo xsd:string.</span><span class="sxs-lookup"><span data-stu-id="dc302-140">Values of the xsd:string type.</span></span>  <br/> |
   

