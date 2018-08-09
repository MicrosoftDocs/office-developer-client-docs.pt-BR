---
title: fld_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: c4ea016adea237258ba699c54bf05b902119eca1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771896"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="48988-102">fld_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="48988-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="48988-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="48988-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48988-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="48988-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="48988-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="48988-105">**Schema file**</span></span> <br/> |<span data-ttu-id="48988-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="48988-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="48988-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="48988-107">**Extension base**</span></span> <br/> |<span data-ttu-id="48988-108">XSD: String</span><span class="sxs-lookup"><span data-stu-id="48988-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48988-109">Definição</span><span class="sxs-lookup"><span data-stu-id="48988-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="48988-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="48988-110">Elements and attributes</span></span>

<span data-ttu-id="48988-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="48988-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="48988-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="48988-112">Child elements</span></span>

<span data-ttu-id="48988-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="48988-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="48988-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="48988-114">Attributes</span></span>

|<span data-ttu-id="48988-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="48988-115">**Attribute**</span></span>|<span data-ttu-id="48988-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="48988-116">**Type**</span></span>|<span data-ttu-id="48988-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="48988-117">**Required**</span></span>|<span data-ttu-id="48988-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="48988-118">**Description**</span></span>|<span data-ttu-id="48988-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="48988-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="48988-120">IX</span><span class="sxs-lookup"><span data-stu-id="48988-120">IX</span></span>  <br/> |<span data-ttu-id="48988-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="48988-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="48988-122">obrigatório</span><span class="sxs-lookup"><span data-stu-id="48988-122">required</span></span>  <br/> ||<span data-ttu-id="48988-123">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="48988-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

