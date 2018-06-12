---
title: Trigger_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 38ba2800a32f4f1b4809a5e542fd6b79794bf369
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773177"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="50855-102">Trigger_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="50855-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="50855-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="50855-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50855-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="50855-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="50855-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="50855-105">**Schema file**</span></span> <br/> |<span data-ttu-id="50855-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="50855-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="50855-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="50855-107">**Extension base**</span></span> <br/> |<span data-ttu-id="50855-108">None</span><span class="sxs-lookup"><span data-stu-id="50855-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="50855-109">Definição</span><span class="sxs-lookup"><span data-stu-id="50855-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="50855-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="50855-110">Elements and attributes</span></span>

<span data-ttu-id="50855-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="50855-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="50855-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="50855-112">Child elements</span></span>

|<span data-ttu-id="50855-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="50855-113">**Element**</span></span>|<span data-ttu-id="50855-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="50855-114">**Type**</span></span>|<span data-ttu-id="50855-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50855-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="50855-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="50855-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="50855-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="50855-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="50855-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="50855-118">Attributes</span></span>

|<span data-ttu-id="50855-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="50855-119">**Attribute**</span></span>|<span data-ttu-id="50855-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="50855-120">**Type**</span></span>|<span data-ttu-id="50855-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="50855-121">**Required**</span></span>|<span data-ttu-id="50855-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="50855-122">**Description**</span></span>|<span data-ttu-id="50855-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="50855-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="50855-124">N</span><span class="sxs-lookup"><span data-stu-id="50855-124">N</span></span>  <br/> |<span data-ttu-id="50855-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="50855-125">xsd:string</span></span>  <br/> |<span data-ttu-id="50855-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="50855-126">required</span></span>  <br/> ||<span data-ttu-id="50855-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="50855-127">Values of the xsd:string type.</span></span>  <br/> |
   

