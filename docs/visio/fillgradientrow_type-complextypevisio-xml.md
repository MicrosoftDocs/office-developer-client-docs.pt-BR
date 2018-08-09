---
title: FillGradientRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 40c88316-4710-b5b4-7be4-e3047474d519
ms.openlocfilehash: 4506c7b313ffbbce67aedbad98db7a78ce42ceaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771888"
---
# <a name="fillgradientrowtype-complextype-visio-xml"></a><span data-ttu-id="f9372-102">FillGradientRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f9372-102">FillGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f9372-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="f9372-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9372-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f9372-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f9372-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="f9372-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f9372-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f9372-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f9372-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="f9372-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f9372-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="f9372-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9372-109">Definição</span><span class="sxs-lookup"><span data-stu-id="f9372-109">Definition</span></span>

```XML
          <xs:complexType name="FillGradientRow_Type">
          
          <xs:complexContent>
          <xs:extension base="IndexedRow_Type">
          <xs:sequence>
    <xs:element name="Cell"  type="Cell_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f9372-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="f9372-110">Elements and attributes</span></span>

<span data-ttu-id="f9372-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="f9372-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f9372-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="f9372-112">Child elements</span></span>

|<span data-ttu-id="f9372-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="f9372-113">**Element**</span></span>|<span data-ttu-id="f9372-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f9372-114">**Type**</span></span>|<span data-ttu-id="f9372-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f9372-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9372-116">Célula</span><span class="sxs-lookup"><span data-stu-id="f9372-116">Cell</span></span>](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="f9372-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="f9372-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f9372-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="f9372-118">Attributes</span></span>

<span data-ttu-id="f9372-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="f9372-119">None.</span></span>
  

