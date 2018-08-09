---
title: Elemento ForeignData (ShapeSheet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59db25bc-0283-6f56-0aa9-9be98a3e9041
description: Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como dados OLE, bitmap ou metarquivo do Windows.
ms.openlocfilehash: d548ce8a6b05f8a9a104aee96c0982c6dbccc417
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771937"
---
# <a name="foreigndata-element-shapesheettype-complextype-visio-xml"></a><span data-ttu-id="b2ef0-103">Elemento ForeignData (ShapeSheet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="b2ef0-103">ForeignData element (ShapeSheet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="b2ef0-104">Contém um BLOB codificado de MIME (Multipurpose Internet Mail Extensions) de dados de imagem, como dados OLE, bitmap ou metarquivo do Windows.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-104">Contains a MIME (Multipurpose Internet Mail Extensions) encoded BLOB of picture data, such as Windows metafile, bitmap, or OLE data.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2ef0-105">Elemento de informações</span><span class="sxs-lookup"><span data-stu-id="b2ef0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2ef0-106">**Tipo de elemento**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="b2ef0-107">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="b2ef0-107">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="b2ef0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="b2ef0-109">**Arquivo de esquema**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="b2ef0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="b2ef0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="b2ef0-111">**Partes do documento**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="b2ef0-112">página # XML, master. XML de #</span><span class="sxs-lookup"><span data-stu-id="b2ef0-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b2ef0-113">Definição</span><span class="sxs-lookup"><span data-stu-id="b2ef0-113">Definition</span></span>

```XML
< xs:element name="ForeignData" type="ForeignData_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="b2ef0-114">Elementos e atributos</span><span class="sxs-lookup"><span data-stu-id="b2ef0-114">Elements and attributes</span></span>

<span data-ttu-id="b2ef0-115">Se o esquema define os requisitos específicos, como a **sequência**, **minOccurs**, **maxOccurs**e **Escolha**, consulte a seção de definição.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="b2ef0-116">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="b2ef0-116">Parent elements</span></span>

|<span data-ttu-id="b2ef0-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-117">**Element**</span></span>|<span data-ttu-id="b2ef0-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-118">**Type**</span></span>|<span data-ttu-id="b2ef0-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2ef0-120">Shape</span><span class="sxs-lookup"><span data-stu-id="b2ef0-120">Shape</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2ef0-121">ShapeSheet_Type</span><span class="sxs-lookup"><span data-stu-id="b2ef0-121">ShapeSheet_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2ef0-122">Contém os elementos que definem a uma forma em um **mestre**, **página**ou elemento de forma do grupo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-122">Contains elements that define a shape in a **Master**, **Page**, or group shape element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="b2ef0-123">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="b2ef0-123">Child elements</span></span>

|<span data-ttu-id="b2ef0-124">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-124">**Element**</span></span>|<span data-ttu-id="b2ef0-125">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-125">**Type**</span></span>|<span data-ttu-id="b2ef0-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b2ef0-127">Rel</span><span class="sxs-lookup"><span data-stu-id="b2ef0-127">Rel</span></span>](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b2ef0-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="b2ef0-128">Rel_Type</span></span>](shapesheet_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="b2ef0-129">Especifica uma relação a uma parte contendo os dados de imagem.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-129">Specifies a relationship to a part containing the image data.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="b2ef0-130">Atributos</span><span class="sxs-lookup"><span data-stu-id="b2ef0-130">Attributes</span></span>

|<span data-ttu-id="b2ef0-131">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-131">**Attribute**</span></span>|<span data-ttu-id="b2ef0-132">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-132">**Type**</span></span>|<span data-ttu-id="b2ef0-133">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-133">**Required**</span></span>|<span data-ttu-id="b2ef0-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-134">**Description**</span></span>|<span data-ttu-id="b2ef0-135">**Valores possíveis**</span><span class="sxs-lookup"><span data-stu-id="b2ef0-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b2ef0-136">CompressionLevel</span><span class="sxs-lookup"><span data-stu-id="b2ef0-136">CompressionLevel</span></span>  <br/> |<span data-ttu-id="b2ef0-137">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="b2ef0-137">xsd:double</span></span>  <br/> |<span data-ttu-id="b2ef0-138">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-138">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-139">Especifica o nível de compactação aplicada ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-139">Specifies the level of compression applied to the file.</span></span> <span data-ttu-id="b2ef0-140">Este atributo só é significativo se os dados externos são um objeto estranho baseado em varredura, de como um arquivo GIF, JPG, PNG, TIFF ou DIB.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-140">This attribute is only meaningful if the foreign data is a raster-based foreign object, such as a DIB, JPG, PNG, TIFF, or GIF file.</span></span>  <br/> |<span data-ttu-id="b2ef0-141">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-141">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-142">CompressionType</span><span class="sxs-lookup"><span data-stu-id="b2ef0-142">CompressionType</span></span>  <br/> |<span data-ttu-id="b2ef0-143">XSD:token</span><span class="sxs-lookup"><span data-stu-id="b2ef0-143">xsd:token</span></span>  <br/> |<span data-ttu-id="b2ef0-144">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-144">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-145">Especifica o tipo de compactação aplicada ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-145">Specifies the type of compression applied to the file.</span></span> <span data-ttu-id="b2ef0-146">Este atributo só é significativo se os dados externos são um objeto estranho baseado em varredura, de como um arquivo GIF, JPG, PNG, TIFF ou DIB</span><span class="sxs-lookup"><span data-stu-id="b2ef0-146">This attribute is only meaningful if the foreign data is a raster-based foreign object, such as a DIB, JPG, PNG, TIFF, or GIF file</span></span>  <br/> |<span data-ttu-id="b2ef0-147">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-147">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-148">ExtentX</span><span class="sxs-lookup"><span data-stu-id="b2ef0-148">ExtentX</span></span>  <br/> |<span data-ttu-id="b2ef0-149">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="b2ef0-149">xsd:double</span></span>  <br/> |<span data-ttu-id="b2ef0-150">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-150">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-151">Especifica a extensão horizontal do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-151">Specifies the horizontal extent of the metafile.</span></span> <span data-ttu-id="b2ef0-152">Este atributo só é significativo se os dados externos forem um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-152">This attribute is only meaningful if the foreign data is a metafile.</span></span>  <br/> |<span data-ttu-id="b2ef0-153">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-153">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-154">ExtentY</span><span class="sxs-lookup"><span data-stu-id="b2ef0-154">ExtentY</span></span>  <br/> |<span data-ttu-id="b2ef0-155">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="b2ef0-155">xsd:double</span></span>  <br/> |<span data-ttu-id="b2ef0-156">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-156">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-157">Especifica a extensão vertical do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-157">Specifies the vertical extent of the metafile.</span></span> <span data-ttu-id="b2ef0-158">Este atributo só é significativo se os dados externos forem um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-158">This attribute is only meaningful if the foreign data is a metafile.</span></span>  <br/> |<span data-ttu-id="b2ef0-159">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-159">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-160">ForeignType</span><span class="sxs-lookup"><span data-stu-id="b2ef0-160">ForeignType</span></span>  <br/> |<span data-ttu-id="b2ef0-161">XSD:token</span><span class="sxs-lookup"><span data-stu-id="b2ef0-161">xsd:token</span></span>  <br/> |<span data-ttu-id="b2ef0-162">obrigatório</span><span class="sxs-lookup"><span data-stu-id="b2ef0-162">required</span></span>  <br/> |<span data-ttu-id="b2ef0-163">Indica o tipo de Bitmap, objeto ou tinta metarquivo, EnhMetaFile.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-163">Indicates metafile, EnhMetaFile, Bitmap, Object, or Ink type.</span></span>  <br/> |<span data-ttu-id="b2ef0-164">Valores do tipo xsd:token.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-164">Values of the xsd:token type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-165">MappingMode</span><span class="sxs-lookup"><span data-stu-id="b2ef0-165">MappingMode</span></span>  <br/> |<span data-ttu-id="b2ef0-166">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b2ef0-166">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b2ef0-167">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-167">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-168">Especifica o modo de mapeamento de metarquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-168">Specifies the metafile mapping mode.</span></span> <span data-ttu-id="b2ef0-169">Este atributo só é significativo se os dados externos forem um metarquivo.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-169">This attribute is only meaningful if the foreign data is a metafile.</span></span>  <br/> |<span data-ttu-id="b2ef0-170">Valores do tipo xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-170">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-171">ObjectHeight</span><span class="sxs-lookup"><span data-stu-id="b2ef0-171">ObjectHeight</span></span>  <br/> |<span data-ttu-id="b2ef0-172">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="b2ef0-172">xsd:double</span></span>  <br/> |<span data-ttu-id="b2ef0-173">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-173">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-174">Especifica a altura do objeto em unidades de página.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-174">Specifies the height of the object in page units.</span></span> <span data-ttu-id="b2ef0-175">Este atributo só é significativo se os dados externos são um objeto incorporado do OLE2.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-175">This attribute is only meaningful if the foreign data is an OLE2 embedded object.</span></span>  <br/> |<span data-ttu-id="b2ef0-176">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-176">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-177">ObjectType</span><span class="sxs-lookup"><span data-stu-id="b2ef0-177">ObjectType</span></span>  <br/> |<span data-ttu-id="b2ef0-178">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="b2ef0-178">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="b2ef0-179">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-179">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-180">Um indicador de inteiro do tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-180">An integer indicator of object type.</span></span> <span data-ttu-id="b2ef0-181">Usado quando o tipo estrangeiro é object.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-181">Used when Foreign type is object.</span></span>  <br/> |<span data-ttu-id="b2ef0-182">Valores do tipo xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-182">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-183">ObjectWidth</span><span class="sxs-lookup"><span data-stu-id="b2ef0-183">ObjectWidth</span></span>  <br/> |<span data-ttu-id="b2ef0-184">XSD:Double</span><span class="sxs-lookup"><span data-stu-id="b2ef0-184">xsd:double</span></span>  <br/> |<span data-ttu-id="b2ef0-185">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-185">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-186">Especifica a largura do objeto em unidades de página.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-186">Specifies the width of the object in page units.</span></span> <span data-ttu-id="b2ef0-187">Este atributo só é significativo se os dados externos são um objeto incorporado do OLE2.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-187">This attribute is only meaningful if the foreign data is an OLE2 embedded object.</span></span>  <br/> |<span data-ttu-id="b2ef0-188">Valores do tipo xsd:double.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-188">Values of the xsd:double type.</span></span>  <br/> |
|<span data-ttu-id="b2ef0-189">ShowAsIcon</span><span class="sxs-lookup"><span data-stu-id="b2ef0-189">ShowAsIcon</span></span>  <br/> |<span data-ttu-id="b2ef0-190">XSD:Boolean</span><span class="sxs-lookup"><span data-stu-id="b2ef0-190">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b2ef0-191">opcional</span><span class="sxs-lookup"><span data-stu-id="b2ef0-191">optional</span></span>  <br/> |<span data-ttu-id="b2ef0-192">Indica se deve mostrar ou não mostrar dados incorporados como um ícone.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-192">Indicates whether to show or not show embedded data as an icon.</span></span>  <br/> |<span data-ttu-id="b2ef0-193">Valores do tipo xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="b2ef0-193">Values of the xsd:boolean type.</span></span>  <br/> |
   
