---
title: LineGradientRow_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b35d58b-ec6f-9b99-01fb-c665630e65d7
ms.openlocfilehash: e48172e8213359244a61716d208b8b98776429af
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397370"
---
# <a name="linegradientrowtype-complextype-visio-xml"></a><span data-ttu-id="41bf3-102">LineGradientRow_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="41bf3-102">LineGradientRow_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="41bf3-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="41bf3-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41bf3-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="41bf3-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="41bf3-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="41bf3-105">**Schema file**</span></span> <br/> |<span data-ttu-id="41bf3-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="41bf3-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="41bf3-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="41bf3-107">**Extension base**</span></span> <br/> |<span data-ttu-id="41bf3-108">IndexedRow_Type</span><span class="sxs-lookup"><span data-stu-id="41bf3-108">IndexedRow_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="41bf3-109">Definição</span><span class="sxs-lookup"><span data-stu-id="41bf3-109">Definition</span></span>

```XML
          <xs:complexType name="LineGradientRow_Type">
          
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

## <a name="elements-and-attributes"></a><span data-ttu-id="41bf3-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="41bf3-110">Elements and attributes</span></span>

<span data-ttu-id="41bf3-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="41bf3-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="41bf3-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="41bf3-112">Child elements</span></span>

|<span data-ttu-id="41bf3-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="41bf3-113">**Element**</span></span>|<span data-ttu-id="41bf3-114">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="41bf3-114">**Type**</span></span>|<span data-ttu-id="41bf3-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="41bf3-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="41bf3-116">Célula</span><span class="sxs-lookup"><span data-stu-id="41bf3-116">Cell</span></span>](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[<span data-ttu-id="41bf3-117">Cell_Type</span><span class="sxs-lookup"><span data-stu-id="41bf3-117">Cell_Type</span></span>](cell_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="41bf3-118">Atributos</span><span class="sxs-lookup"><span data-stu-id="41bf3-118">Attributes</span></span>

<span data-ttu-id="41bf3-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="41bf3-119">None.</span></span>
  

