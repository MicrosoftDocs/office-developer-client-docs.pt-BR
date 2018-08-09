---
title: FooterMargin_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: f2cfa7c9d27940308c95318f8a743a4bdd6cb45f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771930"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="39857-102">FooterMargin_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="39857-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="39857-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="39857-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="39857-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="39857-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="39857-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="39857-105">**Schema file**</span></span> <br/> |<span data-ttu-id="39857-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="39857-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="39857-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="39857-107">**Extension base**</span></span> <br/> |<span data-ttu-id="39857-108">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="39857-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="39857-109">Definição</span><span class="sxs-lookup"><span data-stu-id="39857-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="39857-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="39857-110">Elements and attributes</span></span>

<span data-ttu-id="39857-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="39857-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="39857-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="39857-112">Child elements</span></span>

<span data-ttu-id="39857-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="39857-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="39857-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="39857-114">Attributes</span></span>

|<span data-ttu-id="39857-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="39857-115">**Attribute**</span></span>|<span data-ttu-id="39857-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="39857-116">**Type**</span></span>|<span data-ttu-id="39857-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="39857-117">**Required**</span></span>|<span data-ttu-id="39857-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39857-118">**Description**</span></span>|<span data-ttu-id="39857-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="39857-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="39857-120">Unidade</span><span class="sxs-lookup"><span data-stu-id="39857-120">Unit</span></span>  <br/> |<span data-ttu-id="39857-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="39857-121">xsd:string</span></span>  <br/> |<span data-ttu-id="39857-122">opcional</span><span class="sxs-lookup"><span data-stu-id="39857-122">optional</span></span>  <br/> ||<span data-ttu-id="39857-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="39857-123">Values of the xsd:string type.</span></span>  <br/> |
   

