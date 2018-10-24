---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72f252791e374ed4b9b2a40c9b151ef2b91fefe6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588052"
---
# <a name="attmapiprops"></a><span data-ttu-id="6608f-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="6608f-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="6608f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6608f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6608f-105">O atributo **attMAPIProps** é especial ele pode ser usado para codificar qualquer propriedade MAPI que não tem um equivalente no conjunto de atributos definidos pelo TNEF existentes.</span><span class="sxs-lookup"><span data-stu-id="6608f-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="6608f-106">Os dados de atributo são um conjunto contado das propriedades MAPI formatado de ponta a ponta.</span><span class="sxs-lookup"><span data-stu-id="6608f-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="6608f-107">O formato dessa codificação, que permite a qualquer conjunto de propriedades MAPI, é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6608f-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="6608f-108">_Property_Seq:_</span><span class="sxs-lookup"><span data-stu-id="6608f-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="6608f-109">Contagem de propriedade _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="6608f-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="6608f-110">Deve haver quantos itens _Property_Value_ indica o valor de contagem de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6608f-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="6608f-111">_Property_Value:_</span><span class="sxs-lookup"><span data-stu-id="6608f-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="6608f-112">marca a propriedade tag-_Property_property _Propriedade Proptag_Name_</span><span class="sxs-lookup"><span data-stu-id="6608f-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="6608f-113">A marca de propriedade é simplesmente o valor associado com o identificador de propriedade, como 0x0037001F para **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6608f-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="6608f-114">_Propriedade:_</span><span class="sxs-lookup"><span data-stu-id="6608f-114">_Property:_</span></span>
  
>  <span data-ttu-id="6608f-115">Valor-contagem de _valor_ _valor,..._</span><span class="sxs-lookup"><span data-stu-id="6608f-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="6608f-116">_Valor:_</span><span class="sxs-lookup"><span data-stu-id="6608f-116">_Value:_</span></span>
  
> <span data-ttu-id="6608f-117">tamanho do valor de dados do valor valor-dados preenchimento de dados do valor do tamanho do valor valor-IID de preenchimento</span><span class="sxs-lookup"><span data-stu-id="6608f-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="6608f-118">_Proptag_Name:_</span><span class="sxs-lookup"><span data-stu-id="6608f-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="6608f-119">preenchimento de cadeia de caracteres de nome de comprimento da cadeia de caracteres de nome do guid de nome nome-guid de id de nome de tipo de nome tipo de nome</span><span class="sxs-lookup"><span data-stu-id="6608f-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="6608f-120">O encapsulamento de cada propriedade varia de acordo com o identificador de propriedade e o tipo de propriedade.</span><span class="sxs-lookup"><span data-stu-id="6608f-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="6608f-121">Tipos e identificadores de marcas de propriedade são definidos nos arquivos de cabeçalho Mapitags.h e Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="6608f-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="6608f-122">Se a propriedade for uma propriedade com nome, a marca de propriedade é imediatamente seguida pelo nome da propriedade MAPI, consistindo em um identificador global exclusivo (GUID), um tipo e um identificador ou uma cadeia de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6608f-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="6608f-123">Vários valores de propriedades e valores de comprimento variável, como os tipos de propriedade PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, são tratados da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="6608f-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="6608f-124">Primeiro o número de valores, codificadas como de 32 bits não assinados longas é colocado no stream TNEF, seguido por valores individuais.</span><span class="sxs-lookup"><span data-stu-id="6608f-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="6608f-125">Dados do valor de cada propriedade é codificado como seu tamanho em bytes, seguido dos dados de valor em si.</span><span class="sxs-lookup"><span data-stu-id="6608f-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="6608f-126">Os dados do valor é preenchido a um limite de 4 bytes, embora a quantidade de preenchimento não está incluída no tamanho do valor.</span><span class="sxs-lookup"><span data-stu-id="6608f-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="6608f-127">Se a propriedade for do tipo PT_OBJECT, o tamanho do valor é seguido pelo identificador de interface do objeto.</span><span class="sxs-lookup"><span data-stu-id="6608f-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="6608f-128">A implementação atual do TNEF suporta apenas os identificadores de interface IID_IMessage, IID_IStorage e IID_Istream.</span><span class="sxs-lookup"><span data-stu-id="6608f-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="6608f-129">O tamanho do identificador de interface é incluído no valor-tamanho.</span><span class="sxs-lookup"><span data-stu-id="6608f-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="6608f-130">Se o objeto for uma mensagem incorporada (ou seja, tem um tipo de propriedade de PT_OBJECT e um identificador de interface de IID_Imessage), os dados do valor são codificados como um fluxo TNEF incorporado.</span><span class="sxs-lookup"><span data-stu-id="6608f-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="6608f-131">A codificação real de uma mensagem incorporada na implementação de TNEF é feita abrindo um segundo objeto TNEF para o fluxo de original e o embutido de fluxo de processamento.</span><span class="sxs-lookup"><span data-stu-id="6608f-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

