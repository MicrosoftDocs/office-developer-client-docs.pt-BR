---
title: Trigger_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396327"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="74e9c-102">Trigger_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="74e9c-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="74e9c-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="74e9c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="74e9c-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="74e9c-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="74e9c-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="74e9c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="74e9c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="74e9c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="74e9c-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="74e9c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="74e9c-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="74e9c-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="74e9c-109">Definição</span><span class="sxs-lookup"><span data-stu-id="74e9c-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="74e9c-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="74e9c-110">Elements and attributes</span></span>

<span data-ttu-id="74e9c-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="74e9c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="74e9c-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="74e9c-112">Child elements</span></span>

|<span data-ttu-id="74e9c-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="74e9c-113">**Element**</span></span>|<span data-ttu-id="74e9c-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="74e9c-114">**Type**</span></span>|<span data-ttu-id="74e9c-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="74e9c-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="74e9c-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="74e9c-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="74e9c-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="74e9c-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="74e9c-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="74e9c-118">Attributes</span></span>

|<span data-ttu-id="74e9c-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="74e9c-119">**Attribute**</span></span>|<span data-ttu-id="74e9c-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="74e9c-120">**Type**</span></span>|<span data-ttu-id="74e9c-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="74e9c-121">**Required**</span></span>|<span data-ttu-id="74e9c-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="74e9c-122">**Description**</span></span>|<span data-ttu-id="74e9c-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="74e9c-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="74e9c-124">N</span><span class="sxs-lookup"><span data-stu-id="74e9c-124">N</span></span>  <br/> |<span data-ttu-id="74e9c-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="74e9c-125">xsd:string</span></span>  <br/> |<span data-ttu-id="74e9c-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="74e9c-126">required</span></span>  <br/> ||<span data-ttu-id="74e9c-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="74e9c-127">Values of the xsd:string type.</span></span>  <br/> |
   

