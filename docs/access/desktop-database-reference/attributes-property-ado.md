---
<span data-ttu-id="ec531-101"><<<<<<< Título cabeça: TOCTitle da propriedade Attributes (ADO): propriedade Attributes (ADO) === título: (ADO) da propriedade Attributes TOCTitle: os atributos de propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec531-101"><<<<<<< HEAD title: Attributes Property (ADO) TOCTitle: Attributes Property (ADO) ======= title: Attributes property (ADO) TOCTitle: Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ec531-102">ms:assetid de mestre: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: ms.date 48544716: 18/09/2015 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="ec531-102">master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="ec531-103">ado210.chm1231117 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="ec531-103">ado210.chm1231117 f1_categories:</span></span>
- <span data-ttu-id="ec531-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="ec531-104">Office.Version=v15</span></span>
---

<span data-ttu-id="ec531-105"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ec531-105"><<<<<<< HEAD</span></span>
# <a name="attributes-property-ado"></a><span data-ttu-id="ec531-106">Propriedade Attributes (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec531-106">Attributes Property (ADO)</span></span>
=======
# <a name="attributes-property-ado"></a><span data-ttu-id="ec531-107">Propriedade Attributes (ADO)</span><span class="sxs-lookup"><span data-stu-id="ec531-107">Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="ec531-108">mestre</span><span class="sxs-lookup"><span data-stu-id="ec531-108">master</span></span>


<span data-ttu-id="ec531-109">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec531-109">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="ec531-110">Propriedade Attributes</span><span class="sxs-lookup"><span data-stu-id="ec531-110">Attributes Property</span></span>

<span data-ttu-id="ec531-111">Indica uma ou mais características de um objeto.</span><span class="sxs-lookup"><span data-stu-id="ec531-111">Indicates one or more characteristics of an object.</span></span>

<span data-ttu-id="ec531-112"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="ec531-112"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ec531-113">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ec531-113">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ec531-114">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="ec531-114">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ec531-115">mestre</span><span class="sxs-lookup"><span data-stu-id="ec531-115">master</span></span>

<span data-ttu-id="ec531-116">Define ou retorna um valor **Long**.</span><span class="sxs-lookup"><span data-stu-id="ec531-116">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="ec531-p101">Em um objeto [Connection](connection-object-ado.md), a propriedade **Attributes** é leitura/gravação e seu valor pode ser a soma de um ou mais valores [XactAttributeEnum](xactattributeenum.md). O padrão é zero (0).</span><span class="sxs-lookup"><span data-stu-id="ec531-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="ec531-p102">Em um objeto [Parameter](parameter-object-ado.md), a propriedade **Attributes** é leitura/gravação e seu valor pode ser a soma de um ou mais valores [ParameterAttributesEnum](parameterattributesenum.md). O padrão é **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="ec531-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="ec531-p103">Em um objeto [Field](field-object-ado.md), a propriedade **Attributes** pode ser a soma de um ou mais valores [FieldAttributeEnum](fieldattributeenum.md). Normalmente, ela é somente leitura. Contudo, para novos objetos **Field** que tenham sido acrescentados à coleção [Field](fields-collection-ado.md) de um [Record](record-object-ado.md), **Attributes** será leitura/gravação apenas depois que a propriedade [Value](value-property-ado.md) para o **Field** tiver sido especificada e o novo **Field** tiver sido adicionado com sucesso pelo provedor de dados chamando o método [Update](update-method-ado.md) da coleção **Fields**.</span><span class="sxs-lookup"><span data-stu-id="ec531-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="ec531-123">Em um objeto [Property](property-object-ado.md), a propriedade **Attributes** é somente leitura e seu valor pode ser a soma de um ou mais valores [PropertyAttributesEnum](propertyattributesenum.md).</span><span class="sxs-lookup"><span data-stu-id="ec531-123">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec531-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ec531-124">Remarks</span></span>

<span data-ttu-id="ec531-125">Use a propriedade **Attributes** para definir ou retornar características de objetos **Connection**, **Parameter**, [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ec531-125">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="ec531-p104">Quando vários atributos são definidos, é possível somar as constantes adequadas. A definição do valor de propriedade para uma soma, incluindo constantes incompatíveis, provocará um erro.</span><span class="sxs-lookup"><span data-stu-id="ec531-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="ec531-128">**Uso de serviço de dados remotos** Essa propriedade não está disponível em um objeto de **Conexão** do cliente.</span><span class="sxs-lookup"><span data-stu-id="ec531-128">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

