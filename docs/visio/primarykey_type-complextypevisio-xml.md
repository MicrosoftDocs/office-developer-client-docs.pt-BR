---
title: PrimaryKey_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 679c6335d89855febd82bdeb6e9ac88f4089e1c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391364"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="9ebcd-102">PrimaryKey_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9ebcd-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9ebcd-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="9ebcd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ebcd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9ebcd-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9ebcd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="9ebcd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9ebcd-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9ebcd-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9ebcd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ebcd-109">Definição</span><span class="sxs-lookup"><span data-stu-id="9ebcd-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ebcd-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="9ebcd-110">Elements and attributes</span></span>

<span data-ttu-id="9ebcd-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9ebcd-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="9ebcd-112">Child elements</span></span>

|<span data-ttu-id="9ebcd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-113">**Element**</span></span>|<span data-ttu-id="9ebcd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-114">**Type**</span></span>|<span data-ttu-id="9ebcd-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ebcd-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="9ebcd-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="9ebcd-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="9ebcd-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="9ebcd-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="9ebcd-118">Attributes</span></span>

|<span data-ttu-id="9ebcd-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-119">**Attribute**</span></span>|<span data-ttu-id="9ebcd-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-120">**Type**</span></span>|<span data-ttu-id="9ebcd-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-121">**Required**</span></span>|<span data-ttu-id="9ebcd-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-122">**Description**</span></span>|<span data-ttu-id="9ebcd-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="9ebcd-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ebcd-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="9ebcd-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="9ebcd-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="9ebcd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="9ebcd-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="9ebcd-126">required</span></span>  <br/> ||<span data-ttu-id="9ebcd-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="9ebcd-127">Values of the xsd:string type.</span></span>  <br/> |
   

