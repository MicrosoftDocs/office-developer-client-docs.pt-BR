---
title: UserRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae2e014b-2e53-c317-0bfa-9a0cb1e09588
ms.openlocfilehash: 0d670ecdc9230843cffb0336f3f4ad5c53285615
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773242"
---
# <a name="userrowtype-complextype-visio-xml"></a><span data-ttu-id="41892-102">UserRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="41892-102">UserRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="41892-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="41892-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41892-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="41892-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="41892-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="41892-105">**Schema file**</span></span> <br/> |<span data-ttu-id="41892-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="41892-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="41892-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="41892-107">**Extension base**</span></span> <br/> |<span data-ttu-id="41892-108">NamedRow_Type</span><span class="sxs-lookup"><span data-stu-id="41892-108">NamedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="41892-109">Definição</span><span class="sxs-lookup"><span data-stu-id="41892-109">Definition</span></span>

```XML
          <xs:complexType name="UserRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="41892-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="41892-110">Elements and attributes</span></span>

<span data-ttu-id="41892-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="41892-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="41892-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="41892-112">Child elements</span></span>

|<span data-ttu-id="41892-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="41892-113">**Element**</span></span>|<span data-ttu-id="41892-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="41892-114">**Type**</span></span>|<span data-ttu-id="41892-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41892-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="41892-116">Célula</span><span class="sxs-lookup"><span data-stu-id="41892-116">Cell</span></span>](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[<span data-ttu-id="41892-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="41892-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="41892-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="41892-118">Attributes</span></span>

<span data-ttu-id="41892-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="41892-119">None.</span></span>
  

