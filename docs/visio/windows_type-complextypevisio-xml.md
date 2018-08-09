---
title: Windows_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 33a2acaad76543115c480b5e9a32ddba8fb0d66a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773284"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="85575-102">Windows_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="85575-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="85575-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="85575-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85575-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85575-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="85575-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="85575-105">**Schema file**</span></span> <br/> |<span data-ttu-id="85575-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="85575-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="85575-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="85575-107">**Extension base**</span></span> <br/> |<span data-ttu-id="85575-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="85575-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85575-109">Definição</span><span class="sxs-lookup"><span data-stu-id="85575-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="85575-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="85575-110">Elements and attributes</span></span>

<span data-ttu-id="85575-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="85575-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85575-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="85575-112">Child elements</span></span>

|<span data-ttu-id="85575-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="85575-113">**Element**</span></span>|<span data-ttu-id="85575-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85575-114">**Type**</span></span>|<span data-ttu-id="85575-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85575-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85575-116">Window</span><span class="sxs-lookup"><span data-stu-id="85575-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="85575-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="85575-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="85575-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="85575-118">Attributes</span></span>

|<span data-ttu-id="85575-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="85575-119">**Attribute**</span></span>|<span data-ttu-id="85575-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="85575-120">**Type**</span></span>|<span data-ttu-id="85575-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="85575-121">**Required**</span></span>|<span data-ttu-id="85575-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="85575-122">**Description**</span></span>|<span data-ttu-id="85575-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="85575-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85575-124">Propriedades ClientHeight</span><span class="sxs-lookup"><span data-stu-id="85575-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="85575-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="85575-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="85575-126">opcional</span><span class="sxs-lookup"><span data-stu-id="85575-126">optional</span></span>  <br/> ||<span data-ttu-id="85575-127">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="85575-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="85575-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="85575-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="85575-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="85575-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="85575-130">opcional</span><span class="sxs-lookup"><span data-stu-id="85575-130">optional</span></span>  <br/> ||<span data-ttu-id="85575-131">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="85575-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

