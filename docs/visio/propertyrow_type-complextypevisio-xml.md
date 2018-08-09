---
title: PropertyRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 813d6dee-b113-c0c9-3f53-c5bfd05b92f2
ms.openlocfilehash: 4093f0e826fabc3f732f71b91beaf0ad40f8c54c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772621"
---
# <a name="propertyrowtype-complextype-visio-xml"></a><span data-ttu-id="4165d-102">PropertyRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="4165d-102">PropertyRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4165d-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="4165d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4165d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4165d-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4165d-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="4165d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4165d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4165d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4165d-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="4165d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4165d-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="4165d-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4165d-109">Definição</span><span class="sxs-lookup"><span data-stu-id="4165d-109">Definition</span></span>

```XML
          <xs:complexType name="PropertyRow_Type">
          
          <xs:complexContent>
          <xs:extension base="NamedRow_Type">
          <xs:all>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:all>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4165d-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="4165d-110">Elements and attributes</span></span>

<span data-ttu-id="4165d-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="4165d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4165d-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="4165d-112">Child elements</span></span>

|<span data-ttu-id="4165d-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4165d-113">**Element**</span></span>|<span data-ttu-id="4165d-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="4165d-114">**Type**</span></span>|<span data-ttu-id="4165d-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4165d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4165d-116">Célula</span><span class="sxs-lookup"><span data-stu-id="4165d-116">Cell</span></span>](cell-element-shape-data-sectionvisio-xml.md) <br/> |[<span data-ttu-id="4165d-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="4165d-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4165d-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="4165d-118">Attributes</span></span>

<span data-ttu-id="4165d-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="4165d-119">None.</span></span>
  

