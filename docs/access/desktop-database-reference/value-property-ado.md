---
<span data-ttu-id="59857-101"><<<<<<< Título cabeça: valor Property (ADO) TOCTitle: valor de propriedade (ADO) === título: valor de propriedade (ADO) TOCTitle: valor de propriedade (ADO)</span><span class="sxs-lookup"><span data-stu-id="59857-101"><<<<<<< HEAD title: Value Property (ADO) TOCTitle: Value Property (ADO) ======= title: Value property (ADO) TOCTitle: Value property (ADO)</span></span>
>>>>>>> <span data-ttu-id="59857-102">ms:assetid de mestre: ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID: ms.date 48548958: 18/09/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="59857-102">master ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID: 48548958 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="59857-103"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="59857-103"><<<<<<< HEAD</span></span>
# <a name="value-property-ado"></a><span data-ttu-id="59857-104">Propriedade Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="59857-104">Value Property (ADO)</span></span>
=======
# <a name="value-property-ado"></a><span data-ttu-id="59857-105">Propriedade Value (ADO)</span><span class="sxs-lookup"><span data-stu-id="59857-105">Value property (ADO)</span></span>
>>>>>>> <span data-ttu-id="59857-106">mestre</span><span class="sxs-lookup"><span data-stu-id="59857-106">master</span></span>


<span data-ttu-id="59857-107">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="59857-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="59857-108">Indica o valor atribuído a um objeto [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="59857-108">Indicates the value assigned to a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md) object.</span></span>

<span data-ttu-id="59857-109"><<<<<<< Cabeça</span><span class="sxs-lookup"><span data-stu-id="59857-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="59857-110">Configurações e valor de retorno</span><span class="sxs-lookup"><span data-stu-id="59857-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="59857-111">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="59857-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="59857-112">mestre</span><span class="sxs-lookup"><span data-stu-id="59857-112">master</span></span>

<span data-ttu-id="59857-p101">Define ou retorna um valor **Variant** que indica o valor do objeto. O valor padrão depende da propriedade [Type](type-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="59857-p101">Sets or returns a **Variant** value that indicates the value of the object. Default value depends on the [Type](type-property-ado.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="59857-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="59857-115">Remarks</span></span>

<span data-ttu-id="59857-p102">Utilize a propriedade **Value** para definir ou retornar dados a partir dos objetos **Field**, para definir ou retornar valores de parâmetro com os objetos **Parameter**, ou para definir ou retornar definições de propriedade com os objetos **Property**. A definição da propriedade **Value** como leitura/gravação ou somente leitura depende de diversos fatores  consulte os tópicos do respectivo objeto para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="59857-p102">Use the **Value** property to set or return data from **Field** objects, to set or return parameter values with **Parameter** objects, or to set or return property settings with **Property** objects. Whether the **Value** property is read/write or read-only depends upon numerous factors — see the respective object topics for more information.</span></span>

<span data-ttu-id="59857-118">O ADO permite a definição e o retorno de dados binários longos com a propriedade **Value**.</span><span class="sxs-lookup"><span data-stu-id="59857-118">ADO allows setting and returning long binary data with the **Value** property.</span></span>


> [!NOTE]
> <P><span data-ttu-id="59857-p103">[!OBSERVAçãO] Para os objetos <STRONG>Parameter</STRONG>, o ADO lê a propriedade <STRONG>Value</STRONG> somente uma vez a partir do provedor. Se um comando contiver um <STRONG>Parameter</STRONG> cuja propriedade <STRONG>Value</STRONG> esteja vazia e você criar um <A href="recordset-object-ado.md">Recordset</A> a partir do comando, certifique-se de fechar o <STRONG>Recordset</STRONG> antes de recuperar a propriedade <STRONG>Value</STRONG>. Caso contrário, para alguns provedores, a propriedade <STRONG>Value</STRONG> poderá ficar vazia e não conterá o valor correto.</span><span class="sxs-lookup"><span data-stu-id="59857-p103">For <STRONG>Parameter</STRONG> objects, ADO reads the <STRONG>Value</STRONG> property only once from the provider. If a command contains a <STRONG>Parameter</STRONG> whose <STRONG>Value</STRONG> property is empty, and you create a <A href="recordset-object-ado.md">Recordset</A> from the command, ensure that you first close the <STRONG>Recordset</STRONG> before retrieving the <STRONG>Value</STRONG> property. Otherwise, for some providers, the <STRONG>Value</STRONG> property may be empty, and won't contain the correct value.</span></span></P>



<span data-ttu-id="59857-p104">Para novos objetos **Field** que foram acrescentados à coleção [Fields](fields-collection-ado.md) de um objeto [Record](record-object-ado.md), a propriedade **Value** deverá ser definida antes que qualquer outra propriedade **Field** seja especificada. Primeiro, um valor específico para a propriedade **Value** deve ser atribuído e o método [Update](update-method-ado.md) deve ser chamado na coleção **Fields**. Assim, outras propriedades, como [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md), poderão ser acessadas.</span><span class="sxs-lookup"><span data-stu-id="59857-p104">For new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md) object, the **Value** property must be set before any other **Field** properties can be specified. First, a specific value for the **Value** property must have been assigned and [Update](update-method-ado.md) on the **Fields** collection called. Then, other properties such as [Type](type-property-ado.md) or [Attributes](attributes-property-ado.md) can be accessed.</span></span>

