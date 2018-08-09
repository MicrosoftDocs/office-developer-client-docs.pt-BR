---
title: HeaderMargin_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 70b16680446af8973605d24f41b69778a1ec2c2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772017"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="418ce-102">HeaderMargin_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="418ce-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="418ce-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="418ce-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="418ce-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="418ce-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="418ce-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="418ce-105">**Schema file**</span></span> <br/> |<span data-ttu-id="418ce-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="418ce-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="418ce-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="418ce-107">**Extension base**</span></span> <br/> |<span data-ttu-id="418ce-108">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="418ce-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="418ce-109">Definição</span><span class="sxs-lookup"><span data-stu-id="418ce-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="418ce-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="418ce-110">Elements and attributes</span></span>

<span data-ttu-id="418ce-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="418ce-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="418ce-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="418ce-112">Child elements</span></span>

<span data-ttu-id="418ce-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="418ce-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="418ce-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="418ce-114">Attributes</span></span>

|<span data-ttu-id="418ce-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="418ce-115">**Attribute**</span></span>|<span data-ttu-id="418ce-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="418ce-116">**Type**</span></span>|<span data-ttu-id="418ce-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="418ce-117">**Required**</span></span>|<span data-ttu-id="418ce-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="418ce-118">**Description**</span></span>|<span data-ttu-id="418ce-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="418ce-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="418ce-120">Unidade</span><span class="sxs-lookup"><span data-stu-id="418ce-120">Unit</span></span>  <br/> |<span data-ttu-id="418ce-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="418ce-121">xsd:string</span></span>  <br/> |<span data-ttu-id="418ce-122">opcional</span><span class="sxs-lookup"><span data-stu-id="418ce-122">optional</span></span>  <br/> ||<span data-ttu-id="418ce-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="418ce-123">Values of the xsd:string type.</span></span>  <br/> |
   

