---
title: PrimaryKey_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2d13ac2b6d55fdda752f16af28a0843d5a388f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772600"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="f0dfd-102">PrimaryKey_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f0dfd-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f0dfd-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="f0dfd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f0dfd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f0dfd-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f0dfd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f0dfd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f0dfd-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f0dfd-108">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f0dfd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f0dfd-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f0dfd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f0dfd-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f0dfd-110">Elements and attributes</span></span>

<span data-ttu-id="f0dfd-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f0dfd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f0dfd-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f0dfd-112">Child elements</span></span>

|<span data-ttu-id="f0dfd-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-113">**Element**</span></span>|<span data-ttu-id="f0dfd-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-114">**Type**</span></span>|<span data-ttu-id="f0dfd-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f0dfd-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="f0dfd-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f0dfd-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="f0dfd-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f0dfd-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f0dfd-118">Attributes</span></span>

|<span data-ttu-id="f0dfd-119">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-119">**Attribute**</span></span>|<span data-ttu-id="f0dfd-120">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-120">**Type**</span></span>|<span data-ttu-id="f0dfd-121">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-121">**Required**</span></span>|<span data-ttu-id="f0dfd-122">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-122">**Description**</span></span>|<span data-ttu-id="f0dfd-123">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="f0dfd-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f0dfd-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="f0dfd-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="f0dfd-125">XSD: String</span><span class="sxs-lookup"><span data-stu-id="f0dfd-125">xsd:string</span></span>  <br/> |<span data-ttu-id="f0dfd-126">obrigatório</span><span class="sxs-lookup"><span data-stu-id="f0dfd-126">required</span></span>  <br/> ||<span data-ttu-id="f0dfd-127">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f0dfd-127">Values of the xsd:string type.</span></span>  <br/> |
   

