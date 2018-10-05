---
title: Windows_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386555"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="41903-102">Windows_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="41903-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="41903-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="41903-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41903-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="41903-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="41903-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="41903-105">**Schema file**</span></span> <br/> |<span data-ttu-id="41903-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="41903-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="41903-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="41903-107">**Extension base**</span></span> <br/> |<span data-ttu-id="41903-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="41903-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="41903-109">Definição</span><span class="sxs-lookup"><span data-stu-id="41903-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="41903-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="41903-110">Elements and attributes</span></span>

<span data-ttu-id="41903-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="41903-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="41903-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="41903-112">Child elements</span></span>

|<span data-ttu-id="41903-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="41903-113">**Element**</span></span>|<span data-ttu-id="41903-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="41903-114">**Type**</span></span>|<span data-ttu-id="41903-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41903-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="41903-116">Window</span><span class="sxs-lookup"><span data-stu-id="41903-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="41903-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="41903-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="41903-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="41903-118">Attributes</span></span>

|<span data-ttu-id="41903-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="41903-119">**Attribute**</span></span>|<span data-ttu-id="41903-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="41903-120">**Type**</span></span>|<span data-ttu-id="41903-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="41903-121">**Required**</span></span>|<span data-ttu-id="41903-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41903-122">**Description**</span></span>|<span data-ttu-id="41903-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="41903-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="41903-124">Propriedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="41903-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="41903-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="41903-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="41903-126">opcional</span><span class="sxs-lookup"><span data-stu-id="41903-126">optional</span></span>  <br/> ||<span data-ttu-id="41903-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="41903-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="41903-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="41903-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="41903-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="41903-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="41903-130">opcional</span><span class="sxs-lookup"><span data-stu-id="41903-130">optional</span></span>  <br/> ||<span data-ttu-id="41903-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="41903-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

