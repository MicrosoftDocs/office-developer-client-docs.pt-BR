---
title: FooterMargin_Type complexType ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398931"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="af3fb-102">FooterMargin_Type complexType ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="af3fb-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="af3fb-103">Informações de tipo</span><span class="sxs-lookup"><span data-stu-id="af3fb-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="af3fb-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="af3fb-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="af3fb-105">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="af3fb-105">**Schema file**</span></span> <br/> |<span data-ttu-id="af3fb-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="af3fb-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="af3fb-107">**Extensão de base**</span><span class="sxs-lookup"><span data-stu-id="af3fb-107">**Extension base**</span></span> <br/> |<span data-ttu-id="af3fb-108">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="af3fb-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="af3fb-109">Definição</span><span class="sxs-lookup"><span data-stu-id="af3fb-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="af3fb-110">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="af3fb-110">Elements and attributes</span></span>

<span data-ttu-id="af3fb-111">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="af3fb-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="af3fb-112">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="af3fb-112">Child elements</span></span>

<span data-ttu-id="af3fb-113">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="af3fb-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="af3fb-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="af3fb-114">Attributes</span></span>

|<span data-ttu-id="af3fb-115">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="af3fb-115">**Attribute**</span></span>|<span data-ttu-id="af3fb-116">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="af3fb-116">**Type**</span></span>|<span data-ttu-id="af3fb-117">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="af3fb-117">**Required**</span></span>|<span data-ttu-id="af3fb-118">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="af3fb-118">**Description**</span></span>|<span data-ttu-id="af3fb-119">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="af3fb-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="af3fb-120">Unidade</span><span class="sxs-lookup"><span data-stu-id="af3fb-120">Unit</span></span>  <br/> |<span data-ttu-id="af3fb-121">XSD: String</span><span class="sxs-lookup"><span data-stu-id="af3fb-121">xsd:string</span></span>  <br/> |<span data-ttu-id="af3fb-122">opcional</span><span class="sxs-lookup"><span data-stu-id="af3fb-122">optional</span></span>  <br/> ||<span data-ttu-id="af3fb-123">Valores do tipo xsd: String.</span><span class="sxs-lookup"><span data-stu-id="af3fb-123">Values of the xsd:string type.</span></span>  <br/> |
   

